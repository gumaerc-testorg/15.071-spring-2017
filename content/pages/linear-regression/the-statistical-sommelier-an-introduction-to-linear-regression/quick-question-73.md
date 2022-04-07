---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '2.2 The Statistical Sommelier: An Introduction to Linear Regression'
parent_type: CourseSection
parent_uid: 4495fb48-3934-3c33-23b2-2ef2104af559
title: '2.2 The Statistical Sommelier: An Introduction to Linear Regression'
uid: d97e0bd0-54ac-d9a6-df59-9f1b2e2daf73
---

*   {{< resource_link 505bba75-964b-7b2c-74d8-ebcee23c8259 "\<Video 3: Multiple Linear Regression" >}}
*   {{< resource_link 4495fb48-3934-3c33-23b2-2ef2104af559 "2.2.1Video 1: Predicting the Quality of Wine" >}}
*   {{< resource_link ef446456-afa1-894f-834f-a9ae8908c9a2 "2.2.2Quick Question" >}}
*   {{< resource_link 1f0b61bb-a29b-5ee7-5d26-5ed940cc2d1d "2.2.3Video 2: One-Variable Linear Regression" >}}
*   {{< resource_link a15d356c-50bc-b55a-2cbd-e1c66378ef25 "2.2.4Quick Question" >}}
*   {{< resource_link 505bba75-964b-7b2c-74d8-ebcee23c8259 "2.2.5Video 3: Multiple Linear Regression" >}}
*   {{< resource_link d97e0bd0-54ac-d9a6-df59-9f1b2e2daf73 "2.2.6Quick Question" >}}
*   {{< resource_link 9f456e81-561b-ed0d-7c0a-516cd7739d20 "2.2.7Video 4: Linear Regression in R" >}}
*   {{< resource_link dba3745d-05fd-fdd2-c5cc-f0b06194ed26 "2.2.8Quick Question" >}}
*   {{< resource_link 6111ddea-9e02-70be-a097-8feb66c8bf60 "2.2.9Video 5: Understanding the Model" >}}
*   {{< resource_link 20a0ee2d-c563-bbc1-243a-facac65c21f3 "2.2.10Quick Question" >}}
*   {{< resource_link 1ab830be-7abc-5468-421c-996f95e8e252 "2.2.11Video 6: Correlation and Multicollinearity" >}}
*   {{< resource_link bef58e98-6cee-f682-d32a-bfab033deaf6 "2.2.12Quick Question" >}}
*   {{< resource_link 9b500b6f-7f1d-17af-5de0-ab9946895858 "2.2.13Video 7: Making Predictions" >}}
*   {{< resource_link 04ad6920-c418-b28f-1259-8538cd8136cf "2.2.14Quick Question" >}}
*   {{< resource_link df5ef364-59d3-2e3f-98ec-9d920d6c5e1d "2.2.15Video 8: Comparing the Model to the Experts" >}}
*   {{< resource_link 9f456e81-561b-ed0d-7c0a-516cd7739d20 "\>Video 4: Linear Regression in R" >}}

Quick Question
--------------

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;No, the model's R² value can only decrease to 0.81 by adding new variables.&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;No, the model's R² value can not decrease at all by adding new variables. &nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Yes, the R² value could decrease to 0.80.&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

The model's R² value can never decrease from adding new variables to the model. This is due to the fact that it is always possible to set the coefficient for the new variable to zero in the new model. However, this would be the same as the old model. So the only reason to make the coefficient non-zero is if it improves the R² value of the model, since linear regression picks the coefficients to minimize the error terms, which is the same as maximizing the R².{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

*   {{< resource_link 505bba75-964b-7b2c-74d8-ebcee23c8259 "BackVideo 3: Multiple Linear Regression" >}}
*   {{< resource_link 9f456e81-561b-ed0d-7c0a-516cd7739d20 "ContinueVideo 4: Linear Regression in R" >}}