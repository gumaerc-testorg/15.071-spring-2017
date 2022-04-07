---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
parent_type: CourseSection
parent_uid: 3063320a-4175-6b8a-4fa9-892f61b52c0d
title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
uid: d9817f81-c4ac-257a-ed44-548eaa714059
---

*   {{< resource_link f6216265-1257-bdbe-4826-8a5e5b311096 "\<Video 6: ROC Curves" >}}
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
*   {{< resource_link 1e61720e-cc15-0a7b-0c5e-b3fe60c5ffa1 "\>Video 7: Interpreting the Model" >}}

Quick Question
--------------

This question will ask about the following ROC curve:

![]({{< resource_file 27296a79-a843-0f35-b099-68891f4d55bc >}})

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;t = 0.2&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;t = 0.3&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;t = 0.7&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;t = 0.8&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

The threshold 0.7 is best to identify a small group of patients who are receiving the worst care with high confidence, since at this threshold we make very few false positive mistakes, and identify about 35% of the true positives. The threshold t = 0.8 is not a good choice, since it makes about the same number of false positives, but only identifies 10% of the true positives. The thresholds 0.2 and 0.3 both identify more of the true positives, but they make more false positive mistakes, so our confidence decreases.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;t = 0.2&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;t = 0.3&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;t = 0.7&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;t = 0.8&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

The threshold 0.3 is the best choice in this scenerio. The threshold 0.2 also identifies over half of the patients receiving poor care, but it makes many more false positive mistakes. The thresholds 0.7 and 0.8 don't identify at least half of the patients receiving poor care.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

*   {{< resource_link f6216265-1257-bdbe-4826-8a5e5b311096 "BackVideo 6: ROC Curves" >}}
*   {{< resource_link 1e61720e-cc15-0a7b-0c5e-b3fe60c5ffa1 "ContinueVideo 7: Interpreting the Model" >}}