---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '4.3 Keeping an Eye on Healthcare Costs: The D2Hawkeye Story '
parent_type: CourseSection
parent_uid: 52a221dd-c011-90a4-45b1-a393b15cb810
title: '4.3 Keeping an Eye on Healthcare Costs: The D2Hawkeye Story '
uid: c679795e-ed4f-1bd8-079e-7f008721cf38
---

*   {{< resource_link d35731b0-1c7f-7810-2382-bc22abd10118 "\<Video 4: Error Measures" >}}
*   {{< resource_link 52a221dd-c011-90a4-45b1-a393b15cb810 "4.3.1Video 1: The Story of D2Hawkeye" >}}
*   {{< resource_link b553ee70-b40e-de78-9660-c10e2ec8c8fd "4.3.2Quick Question" >}}
*   {{< resource_link 58916a03-dd92-5225-7d47-29cceb2a1a43 "4.3.3Video 2: Claims Data" >}}
*   {{< resource_link 846cd845-33f9-6c02-69a8-260e985eeaf7 "4.3.4Quick Question" >}}
*   {{< resource_link f5fa573c-282c-d989-480a-6234fdec7162 "4.3.5Video 3: The Variables" >}}
*   {{< resource_link 9d93302e-c36e-bcf9-c1a5-286d0ec673ee "4.3.6Quick Question" >}}
*   {{< resource_link d35731b0-1c7f-7810-2382-bc22abd10118 "4.3.7Video 4: Error Measures" >}}
*   {{< resource_link c679795e-ed4f-1bd8-079e-7f008721cf38 "4.3.8Quick Question" >}}
*   {{< resource_link 41da33e5-8a10-b265-e28e-4f6bd320913a "4.3.9Video 5: CART to Predict Cost" >}}
*   {{< resource_link f24d4a21-a158-ad7d-b107-ecfb64ec198f "4.3.10Quick Question" >}}
*   {{< resource_link b189783b-0ca7-287f-248b-0339ea5afbeb "4.3.11Video 6: Claims Data in R" >}}
*   {{< resource_link 954c1e9d-aed9-ccd1-65dd-85e2287df612 "4.3.12Quick Question" >}}
*   {{< resource_link 9f0c1981-6b4e-786a-4cb9-64211da05bf8 "4.3.13Video 7: Baseline Method and Penalty Matrix" >}}
*   {{< resource_link 09222225-3a2b-5d3f-b68d-5398ca2111a9 "4.3.14Quick Question" >}}
*   {{< resource_link 42af8e9a-43f3-ab0e-231b-e7ab1d08c0ca "4.3.15Video 8: Predicting Healthcare Cost in R" >}}
*   {{< resource_link 2f9da0d0-e4ef-29ad-6861-c462ec145784 "4.3.16Quick Question" >}}
*   {{< resource_link bc9ba16d-f4b1-d68b-b2a3-dfc6700cfac3 "4.3.17Video 9: Results" >}}
*   {{< resource_link 41da33e5-8a10-b265-e28e-4f6bd320913a "\>Video 5: CART to Predict Cost" >}}

Quick Question
--------------

The image below shows the penalty error matrix that we discussed in the previous video.

![]({{< resource_file 2d20a1e4-50f8-bd62-006b-f8e20477eb64 >}})

We can interpret this matrix as follows. Suppose the actual outcome for an observation is 3, and we predict 2. We find 3 on the top of the matrix, and go down to the second row (since we forecasted 2). The penalty error for this mistake is 2. If for another observation we predict (forecast) 4, but the actual outcome is 1, that is a penalty error of 3.

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;We predict 5 (very high cost), but the actual outcome is 1 (very low cost).&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;We predict 1 (very low cost), but the actual outcome is 5 (very high cost).&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

The highest cost is 8, which occurs when the forecast is 1 (very low cost), but the actual cost is 5 (very high cost). It would be much worse for us to ignore an actual high cost observation than to accidentally predict high cost for someone who turns out to be low cost.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="true" >}}&nbsp;Mistakes where we predict one cost bucket HIGHER than the actual outcome.&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Mistakes where we predict one cost bucket LOWER than the actual outcome.&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

We are happier with mistakes where we predict one cost bucket higher than the actual outcome, since this just means we are being a little overly cautious.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

*   {{< resource_link d35731b0-1c7f-7810-2382-bc22abd10118 "BackVideo 4: Error Measures" >}}
*   {{< resource_link 41da33e5-8a10-b265-e28e-4f6bd320913a "ContinueVideo 5: CART to Predict Cost" >}}