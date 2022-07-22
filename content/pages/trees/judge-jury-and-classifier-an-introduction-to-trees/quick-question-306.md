---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '4.2 Judge, Jury, and Classifier: An Introduction to Trees '
parent_type: CourseSection
parent_uid: 11f9b44d-c296-0689-414b-8c313764a18d
title: '4.2 Judge, Jury, and Classifier: An Introduction to Trees'
uid: 0be06c80-7e39-cc4e-2808-dc63ffaa5efa
video_metadata:
  youtube_id: null
---
## Quick Question

 

Plot the tree that we created using cross-validation. How many splits does it have?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

If you follow the R commands from the previous video, you can plot the tree with prp(StevensTreeCV).

The tree with the best accuracy only has one split! When we were picking different minbucket parameters before, it seemed like this tree was probably not doing a good job of fitting the data. However, this tree with one split gives us the best out-of-sample accuracy. This reminds us that sometimes the simplest models are the best!

CheckShow Answer

 

- [Back: Video 6: Cross-Validation](./resolveuid/aed8634b040dd1af7abb68e999cb9c43)
- [Continue: Video 7: The Model v. The Experts](./resolveuid/2ca2e4f174a66019fbe68e97bba87376)