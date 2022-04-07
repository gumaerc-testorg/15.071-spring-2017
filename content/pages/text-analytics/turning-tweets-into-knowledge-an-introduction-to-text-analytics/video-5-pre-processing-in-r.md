---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '5.2 Turning Tweets into Knowledge: An Introduction to Text Analytics'
parent_type: CourseSection
parent_uid: aea3bc9c-07f7-3648-65c4-6fec93dd8515
title: '5.2 Turning Tweets into Knowledge: An Introduction to Text Analytics'
uid: 6cb54a0c-457f-eabd-e1b7-dd4d95399d8c
---

*   {{< resource_link 820047e7-15d4-d347-40e0-11a49546196a "\<Quick Question" >}}
*   {{< resource_link aea3bc9c-07f7-3648-65c4-6fec93dd8515 "5.2.1Video 1: Twitter" >}}
*   {{< resource_link 55f5a296-f823-1477-e837-4b3f5b26d21f "5.2.2Video 2: Text Analytics" >}}
*   {{< resource_link e9e9d44a-c8e5-6812-4e52-cdb5056597b7 "5.2.3Quick Question" >}}
*   {{< resource_link f8520c5e-c3cf-3c3f-e046-72b8a73ae3a5 "5.2.4Video 3: Creating the Dataset" >}}
*   {{< resource_link 5e8b108b-e5fd-9320-8fe7-cd8bd5420c69 "5.2.5Quick Question" >}}
*   {{< resource_link d4dd2919-7499-fdd3-dac1-bca9ea53d04c "5.2.6Video 4: Bag of Words" >}}
*   {{< resource_link 820047e7-15d4-d347-40e0-11a49546196a "5.2.7Quick Question" >}}
*   {{< resource_link 6cb54a0c-457f-eabd-e1b7-dd4d95399d8c "5.2.8Video 5: Pre-Processing in R" >}}
*   {{< resource_link 2199fef8-1de9-2125-4a61-069ec69f588e "5.2.9Quick Question" >}}
*   {{< resource_link b8c9ec48-67a6-977e-b31d-b490c342ef38 "5.2.10Video 6: Bag of Words in R" >}}
*   {{< resource_link ef17614f-a013-2a73-a771-05ff3c4311af "5.2.11Quick Question" >}}
*   {{< resource_link 6faa3dc6-2c17-bf81-844b-b5d994e997d9 "5.2.12Video 7: Predicting Sentiment" >}}
*   {{< resource_link c08c448d-ba2f-6d4e-4aa3-a930b6c97c07 "5.2.13Quick Question" >}}
*   {{< resource_link f3a415ff-eba9-ca2d-622f-58bcb8aea03c "5.2.14Video 8: Conclusion" >}}
*   {{< resource_link 2199fef8-1de9-2125-4a61-069ec69f588e "\>Quick Question" >}}

Video 5: Pre-Processing in R
----------------------------

**Note:**  the dataset "tweets.csv" used in the rest of this lecture is not available to OCW users.

In the following video, we ask you to install the "tm" package to perform the pre-processing steps. Due to function changes that occurred after this video was recorded, you will need to run the following command immediately after converting all of the words to lowercase letters (it converts all documents in the corpus to the PlainTextDocument type):

corpus \= tm\_map(corpus, PlainTextDocument)

Then you can continue with the R commands as they are in the video.

{{< resource 27420fff-8aba-cd00-e9e0-b59405fc71cc >}}

Non-Standard Stop Word Lists
----------------------------

If the code length(stopwords("english")) does not return 174 for you, then please run the line of code in [stopwords (TXT) file](./resolveuid/cdd1dacd338e534632e1cc15dec3e47d), which will store the standard stop words in a variable called sw. When removing stop words, use tm\_map(corpus, removeWords, sw) instead of tm\_map(corpus, removeWords, stopwords("english")). 

Language Settings
-----------------

If you downloaded and installed R in a location other than the United States, you might encounter some issues when using the bag of words approach (since the pre-processing tasks used here depend on the English language). To fix this, you will need to type in your R console:

Sys.setlocale("LC\_ALL", "C")

This will only change the locale for your current R session, so please make a note to run this command when you are working on any lectures or exercises that might depend on the English lanugage (for example, removing stop words).

*   {{< resource_link 820047e7-15d4-d347-40e0-11a49546196a "BackQuick Question" >}}
*   {{< resource_link 2199fef8-1de9-2125-4a61-069ec69f588e "ContinueQuick Question" >}}