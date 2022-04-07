---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
parent_type: CourseSection
parent_uid: 3063320a-4175-6b8a-4fa9-892f61b52c0d
title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
uid: 4551bb95-ca82-a0ca-cf08-eda74141daaa
---

*   {{< resource_link a92dcb88-eddd-40ad-72c0-d5bc2288c90e "\<Video 2: Building the Dataset" >}}
*   {{< resource_link 3063320a-4175-6b8a-4fa9-892f61b52c0d "3.2.1Video 1: Replicating Expert Assessment" >}}
*   {{< resource_link a92dcb88-eddd-40ad-72c0-d5bc2288c90e "3.2.2Video 2: Building the Dataset" >}}
*   {{< resource_link 4551bb95-ca82-a0ca-cf08-eda74141daaa "3.2.3Quick Question" >}}
*   {{< resource_link 8099bebb-d4e8-1ce0-9baa-3ede1f3ec357 "3.2.4Video 3: Logistic Regression" >}}
*   {{< resource_link 9cb7a258-ad19-0f7f-84e5-89aad47092b1 "3.2.5Quick Question" >}}
*   {{< resource_link 8fc17cbb-03cd-ce23-b588-0c21e7dc33e8 "3.2.6Video 4: Logistic Regression in R" >}}
*   {{< resource_link 8c080206-9993-5e2b-b0c5-0c4cd73fd74c "3.2.7Quick Question" >}}
*   {{< resource_link 7bf86a6c-2bb6-629e-d20e-4dd216833197 "3.2.8Video 5: Thresholding" >}}
*   {{< resource_link d565e093-b63d-b842-9332-eabcb8503b85 "3.2.9Quick Question" >}}
*   {{< resource_link f6216265-1257-bdbe-4826-8a5e5b311096 "3.2.10Video 6: ROC Curves" >}}
*   {{< resource_link d9817f81-c4ac-257a-ed44-548eaa714059 "3.2.11Quick Question" >}}
*   {{< resource_link 1e61720e-cc15-0a7b-0c5e-b3fe60c5ffa1 "3.2.12Video 7: Interpreting the Model" >}}
*   {{< resource_link 8809159b-6e06-0da2-d386-90c7900fdd67 "3.2.13Quick Question" >}}
*   {{< resource_link 81d5d93d-77c2-b8fc-0b85-d9cbcdc418a5 "3.2.14Video 8: The Analytics Edge" >}}
*   {{< resource_link 8099bebb-d4e8-1ce0-9baa-3ede1f3ec357 "\>Video 3: Logistic Regression" >}}

Quick Question
--------------

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="true" >}}&nbsp;Deciding whether to buy, sell, or hold a stock&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;The weekly revenue of a company &nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;The winner of an election with two candidates&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;The day of the week with the highest revenue&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;The number of daily car thefts in New York City&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;Whether or not revenue will exceed $50,000&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

The weekly revenue of a company is not categorical, since it has a large number of possible values, on a continuous range. The number of daily car thefts in New York City is also not categorical because the number of car thefts could range from 0 to hundreds.

On the other hand, the other options each have a limiited number of possible outcomes.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;Deciding whether to buy, sell, or hold a stock&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;The weekly revenue of a company &nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;The winner of an election with two candidates&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;The day of the week with the highest revenue&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;The number of car thefts in New York City&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;Whether or not revenue will exceed $50,000&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

The only variables with two possible outcomes are the winner of an election with two candidates, and whether or not revenue will exceed $50,000.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

*   {{< resource_link a92dcb88-eddd-40ad-72c0-d5bc2288c90e "BackVideo 2: Building the Dataset" >}}
*   {{< resource_link 8099bebb-d4e8-1ce0-9baa-3ede1f3ec357 "ContinueVideo 3: Logistic Regression" >}}