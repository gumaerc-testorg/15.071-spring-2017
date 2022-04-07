---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '5.4 Predictive Coding: Bringing Text Analytics to the Courtroom  (Recitation)'
parent_type: CourseSection
parent_uid: d4b1a3b9-42ed-98d1-94fe-b3777ba22595
title: '5.4 Predictive Coding: Bringing Text Analytics to the Courtroom  (Recitation)'
uid: 1924c416-bffb-7319-6622-8542170e6c66
---

*   {{< resource_link d2b6e4bc-cf8f-0017-b1fc-3de36e683c9a "\<Video 2: The Data" >}}
*   {{< resource_link d4b1a3b9-42ed-98d1-94fe-b3777ba22595 "5.4.1Welcome to Recitation 5" >}}
*   {{< resource_link 035dbca4-1240-1abd-0c08-bb9c1c3c233d "5.4.2Video 1: The Story of Enron" >}}
*   {{< resource_link d2b6e4bc-cf8f-0017-b1fc-3de36e683c9a "5.4.3Video 2: The Data" >}}
*   {{< resource_link 1924c416-bffb-7319-6622-8542170e6c66 "5.4.4Video 3: Pre-Processing" >}}
*   {{< resource_link 8a96d7cd-01b9-50c8-be68-959be293ab00 "5.4.5Video 4: Bag of Words" >}}
*   {{< resource_link bfe9f689-1834-528b-fc47-66f67aa144c6 "5.4.6Video 5: Building Models" >}}
*   {{< resource_link 54a5cfa0-2012-d081-6815-948514b434c1 "5.4.7Video 6: Evaluating the Model" >}}
*   {{< resource_link 19c7a1c6-b044-e1b2-c2b1-916f5be9f51f "5.4.8Video 7: The ROC Curve" >}}
*   {{< resource_link 452a514d-74e9-b441-d73a-e42c18939bda "5.4.9Video 8: Predictive Coding Today" >}}
*   {{< resource_link 8a96d7cd-01b9-50c8-be68-959be293ab00 "\>Video 4: Bag of Words" >}}

Video 3: Pre-Processing
-----------------------

**Important Note:** In the following video, we ask you to use the "tm" package to perform the pre-processing steps. Due to function changes that occurred after this video was recorded, you will need to run the following command immediately after converting all of the words to lowercase letters (it converts all documents in the corpus to the PlainTextDocument type):

corpus \= tm\_map(corpus, PlainTextDocument)

Then you can continue with the R commands as they are in the video.

{{< resource 4e41dd76-b35c-6d67-c10d-2253c4352758 >}}

If the code length(stopwords("english")) does not return 174 for you, then please run the line of code in [stopwords (TXT) file](./resolveuid/fe588eb69d663b5e0fbdf6c8a2564dfd), which will store the standard stop words in a variable called sw. When removing stop words, use tm\_map(corpus, removeWords, sw) instead of tm\_map(corpus, removeWords, stopwords("english")). 

*   {{< resource_link d2b6e4bc-cf8f-0017-b1fc-3de36e683c9a "BackVideo 2: The Data" >}}
*   {{< resource_link 8a96d7cd-01b9-50c8-be68-959be293ab00 "ContinueVideo 4: Bag of Words" >}}