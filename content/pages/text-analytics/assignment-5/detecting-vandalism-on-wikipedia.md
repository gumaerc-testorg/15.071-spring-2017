---
content_type: page
description: Detecting Vandalism on Wikipedia
draft: false
learning_resource_types:
- Assignments
ocw_type: CourseSection
parent_title: 5.5 Assignment 5
parent_type: CourseSection
parent_uid: 81eae0fd-28f2-8733-6b79-2210ba33dfbb
title: 5.5 Assignment 5
uid: 2e4c9dd9-6d08-4e8f-d1d8-111a5affc5a4
video_metadata:
  youtube_id: null
---
## Detecting Vandalism on Wikipedia

{{% resource_link "9ad3f80d-1ee5-4400-aa46-ff46dd7bbf84" "Wikipedia" %}} is a free online encyclopedia that anyone can edit and contribute to. It is available in many languages and is growing all the time. On the English language version of Wikipedia:

- There are currently {{% resource_link "bdcb8bba-c56f-46ed-9c68-64f9d3233e53" "4.7 million pages" %}}*.*
- *There have been a total over* {{% resource_link "88e654e6-a034-457d-835b-e754af307c71" "*760 million edits*" %}} (also called revisions) over its lifetime.
- There are approximately {{% resource_link "ff56998f-534a-480d-bea3-655bac32b571" "130,000 edits per day" %}}*.*

At time of 15.071x course publication.

One of the consequences of being editable by anyone is that some people *vandalize* pages. This can take the form of removing content, adding promotional or inappropriate content, or more subtle shifts that change the meaning of the article. With this many articles and edits per day it is difficult for humans to detect all instances of vandalism and *revert* (undo) them. As a result, Wikipedia uses *bots* - computer programs that automatically revert edits that look like vandalism. In this assignment we will attempt to develop a vandalism detector that uses machine learning to distinguish between a valid edit and vandalism.

The data for this problem is based on the revision history of the page {{% resource_link "c55c95f1-8dbd-48d1-93bb-354b4ea925d1" "Language" %}}. Wikipedia provides a history for each page that consists of the state of the page at each revision. Rather than manually considering each revision, a script was run that checked whether edits stayed or were reverted. If a change was eventually reverted then that revision is marked as vandalism. This may result in some misclassifications, but the script performs well enough for our needs.

As a result of this preprocessing, some common processing tasks have already been done, including lower-casing and punctuation removal. The columns in the dataset are:

- Vandal = 1 if this edit was vandalism, 0 if not.
- Minor = 1 if the user marked this edit as a "minor edit", 0 if not.
- Loggedin = 1 if the user made this edit while using a Wikipedia account, 0 if they did not.
- Added = The *unique* words added.
- Removed = The *unique* words removed.

Notice the repeated use of *unique*. The data we have available is not the traditional bag of words - rather it is the set of words that were removed or added. For example, if a word was removed multiple times in a revision it will only appear one time in the "Removed" column.

## Problem 1.1 - Bags of Words

Load the data {{% resource_link "689509df-0b61-05e6-af7e-a0b866825c45" "wiki (CSV)" %}} with the option stringsAsFactors=FALSE, calling the data frame "wiki". Convert the "Vandal" column to a factor using the command wiki$Vandal = as.factor(wiki$Vandal).

How many cases of vandalism were detected in the history of this page?

## Problem 1.2 - Bags of Words

We will now use the bag of words approach to build a model. We have two columns of textual data, with different meanings. For example, adding rude words has a different meaning than removing rude words. We'll start like we did in class by building a document term matrix from the Added column. The text already is lowercase and stripped of punctuation. So to pre-process the data, just complete the following four steps:

1) Create the corpus for the Added column, and call it "corpusAdded".

2) Remove the English-language stopwords.

3) Stem the words.

4) Build the DocumentTermMatrix, and call it dtmAdded.

If the code length(stopwords("english")) does not return 174 for you, then please run the line of code in {{% resource_link "8bb9e560-bb61-e719-9ca1-eccfbe6a9832" "stopwords (TXT) file" %}}, which will store the standard stop words in a variable called sw. When removing stop words, use tm\_map(corpusAdded, removeWords, sw) instead of tm\_map(corpusAdded, removeWords, stopwords("english")).

How many terms appear in dtmAdded?

## Problem 1.3 - Bags of Words

Filter out sparse terms by keeping only terms that appear in 0.3% or more of the revisions, and call the new matrix sparseAdded. How many terms appear in sparseAdded?

## Problem 1.4 - Bags of Words

Convert sparseAdded to a data frame called wordsAdded, and then prepend all the words with the letter A, by using the command:

colnames(wordsAdded) = paste("A", colnames(wordsAdded))

Explanation

You need to type the following two commands:

wordsAdded = as.data.frame(as.matrix(sparseAdded))

colnames(wordsAdded) = paste("A", colnames(wordsAdded))

Now repeat all of the steps we've done so far (create a corpus, remove stop words, stem the document, create a sparse document term matrix, and convert it to a data frame) to create a Removed bag-of-words dataframe, called wordsRemoved, except this time, prepend all of the words with the letter R:

colnames(wordsRemoved) = paste("R", colnames(wordsRemoved))

How many words are in the wordsRemoved data frame?

To repeat the steps for the Removed column, use the following commands:

corpusRemoved = Corpus(VectorSource(wiki$Removed))

corpusRemoved = tm\_map(corpusRemoved, removeWords, stopwords("english"))

corpusRemoved = tm\_map(corpusRemoved, stemDocument)

dtmRemoved = DocumentTermMatrix(corpusRemoved)

sparseRemoved = removeSparseTerms(dtmRemoved, 0.997)

wordsRemoved = as.data.frame(as.matrix(sparseRemoved))

colnames(wordsRemoved) = paste("R", colnames(wordsRemoved))

## Problem 1.5 - Bags of Words

Combine the two data frames into a data frame called wikiWords with the following line of code:

wikiWords = cbind(wordsAdded, wordsRemoved)

The cbind function combines two sets of variables for the same observations into one data frame. Then add the Vandal column (HINT: remember how we added the dependent variable back into our data frame in the Twitter lecture). Set the random seed to 123 and then split the data set using sample.split from the "caTools" package to put 70% in the training set.

Explanation

You can combine the two data frames by using the command:

wikiWords = cbind(wordsAdded, wordsRemoved)

And then add the Vandal variable by using the command:

wikiWords$Vandal = wiki$Vandal

To split the data, you can use the following commands:

library(caTools)

set.seed(123)

spl = sample.split(wikiWords$Vandal, SplitRatio = 0.7)

wikiTrain = subset(wikiWords, spl==TRUE)

wikiTest = subset(wikiWords, spl==FALSE)

What is the accuracy on the test set of a baseline method that always predicts "not vandalism" (the most frequent outcome)?

## Problem 1.6 - Bags of Words

Build a CART model to predict Vandal, using all of the other variables as independent variables. Use the training set to build the model and the default parameters (don't set values for minbucket or cp).

What is the accuracy of the model on the test set, using a threshold of 0.5? (Remember that if you add the argument type="class" when making predictions, the output of predict will automatically use a threshold of 0.5.)

## Problem 1.7 - Bags of Words

Plot the CART tree. How many word stems does the CART model use?

## Problem 1.8 - Bags of Words

Given the performance of the CART model relative to the baseline, what is the best explanation of these results?

 We have a bad testing/training split. 

 The CART model overfits to the training set. 

 Although it beats the baseline, bag of words is not very predictive for this problem. 

 We over-sparsified the document-term matrix. 

## Problem 2.1 - Problem-specific Knowledge

We weren't able to improve on the baseline using the raw textual information. More specifically, the words themselves were not useful. There are other options though, and in this section we will try two techniques - identifying a key class of words, and counting words.

The key class of words we will use are website addresses. "Website addresses" (also known as URLs - Uniform Resource Locators) are comprised of two main parts. An example would be "[http://www.google.com"](http://www.google.com/). The first part is the protocol, which is usually "http" (HyperText Transfer Protocol). The second part is the address of the site, e.g. "[www.google.com"](http://www.google.com/). We have stripped all punctuation so links to websites appear in the data as one word, e.g. "httpwwwgooglecom". We hypothesize that given that a lot of vandalism seems to be adding links to promotional or irrelevant websites, the presence of a web address is a sign of vandalism.

We can search for the presence of a web address in the words added by searching for "http" in the Added column. The grepl function returns TRUE if a string is found in another string, e.g.

grepl("cat","dogs and cats",fixed=TRUE) # TRUE

grepl("cat","dogs and rats",fixed=TRUE) # FALSE

Create a copy of your dataframe from the previous question:

wikiWords2 = wikiWords

Make a new column in wikiWords2 that is 1 if "http" was in Added:

wikiWords2$HTTP = ifelse(grepl("http",wiki$Added,fixed=TRUE), 1, 0)

Based on this new column, how many revisions added a link?

## Problem 2.2 - Problem-Specific Knowledge

In problem 1.5, you computed a vector called "spl" that identified the observations to put in the training and testing sets. Use that variable (do not recompute it with sample.split) to make new training and testing sets:

wikiTrain2 = subset(wikiWords2, spl==TRUE)

wikiTest2 = subset(wikiWords2, spl==FALSE)

Then create a new CART model using this new variable as one of the independent variables.

What is the new accuracy of the CART model on the test set, using a threshold of 0.5?

You can compute this by running the following commands:

wikiCART2 = rpart(Vandal ~ ., data=wikiTrain2, method="class")

testPredictCART2 = predict(wikiCART2, newdata=wikiTest2, type="class")

table(wikiTest2$Vandal, testPredictCART2)

## Problem 2.3 - Problem-Specific Knowledge

Another possibility is that the number of words added and removed is predictive, perhaps more so than the actual words themselves. We already have a word count available in the form of the document-term matrices (DTMs).

Sum the rows of dtmAdded and dtmRemoved and add them as new variables in your data frame wikiWords2 (called NumWordsAdded and NumWordsRemoved) by using the following commands:

wikiWords2$NumWordsAdded = rowSums(as.matrix(dtmAdded))

wikiWords2$NumWordsRemoved = rowSums(as.matrix(dtmRemoved))

What is the average number of words added?

## Problem 2.4 - Problem-Specific Knowledge

In problem 1.5, you computed a vector called "spl" that identified the observations to put in the training and testing sets. Use that variable (do not recompute it with sample.split) to make new training and testing sets with wikiWords2. Create the CART model again (using the training set and the default parameters).

What is the new accuracy of the CART model on the test set?

To split the data again, use the following commands:

wikiTrain3 = subset(wikiWords2, spl==TRUE)

wikiTest3 = subset(wikiWords2, spl==FALSE)

You can compute the accuracy of the new CART model with the following commands:

wikiCART3 = rpart(Vandal ~ ., data=wikiTrain3, method="class")

testPredictCART3 = predict(wikiCART3, newdata=wikiTest3, type="class")

table(wikiTest3$Vandal, testPredictCART3)

## Problem 3.1 - Using Non-Textual Data

We have two pieces of "metadata" (data about data) that we haven't yet used. Make a copy of wikiWords2, and call it wikiWords3:

wikiWords3 = wikiWords2

Then add the two original variables Minor and Loggedin to this new data frame:

wikiWords3$Minor = wiki$Minor

wikiWords3$Loggedin = wiki$Loggedin

In problem 1.5, you computed a vector called "spl" that identified the observations to put in the training and testing sets. Use that variable (do not recompute it with sample.split) to make new training and testing sets with wikiWords3.

Explanation

This can be done with the following two commands:

wikiTrain4 = subset(wikiWords3, spl==TRUE)

wikiTest4 = subset(wikiWords3, spl==FALSE)

Build a CART model using all the training data. What is the accuracy of the model on the test set?

This model can be built and evaluated using the following commands:

wikiCART4 = rpart(Vandal ~ ., data=wikiTrain4, method="class")

predictTestCART4 = predict(wikiCART4, newdata=wikiTest4, type="class")

table(wikiTest4$Vandal, predictTestCART4)

## Problem 3.2 - Using Non-Textual Data

There is a substantial difference in the accuracy of the model using the meta data. Is this because we made a more complicated model?

Plot the CART tree. How many splits are there in the tree?

- {{% resource_link "81eae0fd-28f2-8733-6b79-2210ba33dfbb" "Back: Assignment 5" %}}
- {{% resource_link "f9baad34-7f95-6b6f-8608-66551433d510" "Continue: Automating Reviews in Medicine" %}}