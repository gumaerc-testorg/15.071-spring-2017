---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '4.3 Keeping an Eye on Healthcare Costs: The D2Hawkeye Story '
parent_type: CourseSection
parent_uid: 52a221dd-c011-90a4-45b1-a393b15cb810
title: '4.3 Keeping an Eye on Healthcare Costs: The D2Hawkeye Story'
uid: 954c1e9d-aed9-ccd1-65dd-85e2287df612
video_metadata:
  youtube_id: null
---
## Quick Question

 

What is the average age of patients in the training set, ClaimsTrain?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

What proportion of people in the training set (ClaimsTrain) had at least one diagnosis code for diabetes?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

Explanation

Both of these answers can be found by looking at summary(ClaimsTrain). The mean age should be listed under the age variable, and since diabetes is a binary variable, the mean value of diabetes gives the proportion of people with at least one diagnosis code for diabetes.

Alternatively, you could use the mean, table, and nrow functions:

mean(ClaimsTrain$age)

table(ClaimsTrain$diabetes)/nrow(ClaimsTrain)

CheckShow Answer

 

- [Back: Video 6: Claims Data in R](./resolveuid/b189783b0ca7287f248b0339ea5afbeb)
- [Continue: Video 7: Baseline Method and Penalty Matrix](./resolveuid/9f0c19816b4e786a4cb964211da05bf8)