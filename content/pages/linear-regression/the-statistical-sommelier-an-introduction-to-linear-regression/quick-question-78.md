---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '2.2 The Statistical Sommelier: An Introduction to Linear Regression'
parent_type: CourseSection
parent_uid: 4495fb48-3934-3c33-23b2-2ef2104af559
title: '2.2 The Statistical Sommelier: An Introduction to Linear Regression'
uid: dba3745d-05fd-fdd2-c5cc-f0b06194ed26
video_metadata:
  youtube_id: null
---
## Quick Question

In R, use the dataset [wine (CSV)](./resolveuid/314267a9b7ddb86e315b90440aa4f2ad) to create a linear regression model to predict Price using HarvestRain and WinterRain as independent variables. Using the summary output of this model, answer the following questions:

What is the "Multiple R-squared" value of your model?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

What is the coefficient for HarvestRain?

Exercise 2

&nbsp;Numerical Response&nbsp;

 

What is the intercept coefficient?

Exercise 3

&nbsp;Numerical Response&nbsp;

 

Explanation

In R, create the model by typing the following line into your R console:

modelQQ4 = lm(Price ~ HarvestRain + WinterRain, data=wine)

Then, look at the output of summary(modelQQ4). The Multiple R-squared is listed at the bottom of the output, and the coefficients can be found in the coefficients table.

CheckShow Answer

- [Back: Video 4: Linear Regression in R](./resolveuid/9f456e81561bed0d7c0a516cd7739d20)
- [Continue: Video 5: Understanding the Model](./resolveuid/6111ddea9e0270bea0978feb66c8bf60)