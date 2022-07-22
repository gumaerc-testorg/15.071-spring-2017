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
uid: 076a36dd-c951-926f-d5c9-9ccb41e476d9
video_metadata:
  youtube_id: null
---
## Quick Question

Suppose that you have the following CART tree:

![Example of a cart tree.](./resolveuid/b2eea6fba57db424a4844f679aee4bc9)

How many splits are in this tree?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

For which data observations should we predict "Red", according to this tree? Select all that apply.

Exercise 2

&nbsp;If X is less than 60, and Y is any value.&nbsp;

&nbsp;If X is greater than or equal to 60, and Y is greater than or equal to 20.&nbsp;

&nbsp;If X is greater than or equal to 85, and Y is less than 20.&nbsp;

&nbsp;If X is greater than or equal to 60 and less than 85, and Y is less than 20.&nbsp;

 

Explanation

This tree has three splits. The first split says to predict "Red" if X is less than 60, regardless of the value of Y. Otherwise, we move to the second split. The second split says to check the value of Y - if it is greater than or equal to 20, predict "Gray". Otherwise, we move to the third split. This split checks the value of X again. If X is less than 85 (and greater than or equal to 60 by the first split) and Y is less than 20, then we predict "Red". Otherwise, we predict "Gray".

CheckShow Answer

- [Back: Video 2: CART](./resolveuid/fbeabfb3e0a4b479efe5ffb5d7cf5d4a)
- [Continue: Video 3: Splitting and Predictions](./resolveuid/ca1564b0917866a3a00e801c8c9fdbbc)