---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '8.2 Airline Revenue Management: An Introduction to Linear Optimization '
parent_type: CourseSection
parent_uid: 2900efa7-1aff-756d-feba-74c6d16f2d3d
title: '8.2 Airline Revenue Management: An Introduction to Linear Optimization '
uid: 866b08a8-38d4-f694-786a-619e9ebff44b
---

*   {{< resource_link 80f150bc-38fd-0f84-75f7-ccfe876f7744 "\<Video 7: Connecting Flights" >}}
*   {{< resource_link 2900efa7-1aff-756d-feba-74c6d16f2d3d "8.2.1Video 1: Introduction" >}}
*   {{< resource_link 1a99f51a-66ac-8af1-43ed-d5efdd454605 "8.2.2Video 2: A Single Flight" >}}
*   {{< resource_link 3a0381df-ab5e-b38d-f338-52ce8d57f81b "8.2.3Quick Question" >}}
*   {{< resource_link e9725d1b-f88e-acdd-5ae8-cd5e31dbe7cc "8.2.4Video 3: The Problem Formulation" >}}
*   {{< resource_link b7f0594b-3047-a305-cb8a-f6815a526173 "8.2.5Quick Question" >}}
*   {{< resource_link 86a033cc-e142-d448-a8bb-9112a73f89db "8.2.6Video 4: Solving the Problem" >}}
*   {{< resource_link 52678524-d9df-c344-6fc9-97eed6c5a010 "8.2.7Quick Question" >}}
*   {{< resource_link f7f2a67c-b479-6f7b-313d-a3b222582c72 "8.2.8Video 5: Visualizing the Problem" >}}
*   {{< resource_link bcd5d3fe-6076-3847-5182-4e5ef3218335 "8.2.9Quick Question" >}}
*   {{< resource_link f20e206f-20f7-9b3c-410b-c053183afdbb "8.2.10Video 6: Sensitivity Analysis" >}}
*   {{< resource_link 71d3d9d3-2435-5e5d-1972-5596dcc0bf78 "8.2.11Quick Question" >}}
*   {{< resource_link 80f150bc-38fd-0f84-75f7-ccfe876f7744 "8.2.12Video 7: Connecting Flights" >}}
*   {{< resource_link 866b08a8-38d4-f694-786a-619e9ebff44b "8.2.13Quick Question" >}}
*   {{< resource_link 0cd767eb-f8c6-279f-86f2-16e785139b90 "8.2.14Video 8: The Edge of Revenue Management" >}}
*   {{< resource_link 0cd767eb-f8c6-279f-86f2-16e785139b90 "\>Video 8: The Edge of Revenue Management" >}}

Quick Question
--------------

In this quick question, we'll perform some sensitivity analysis on the connecting flights problem.

Previously, we said that American Airlines could market their fares to increase demand. It costs $200 in advertising to increase demand by one unit.

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;Yes. American Airlines should market the discount fares from JFK to DFW to increase demand by 50.&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Yes. American Airlines should market the discount fares from JFK to DFW to increase demand by 10.&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;No. American Airlines should not market the discount fares from JFK to DFW because even though the revenue increases, it does not exceed the costs.&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;No. American Airlines should not market the discount fares from JFK to DFW because the revenue does not increase at all by increasing the demand for these tickets.&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

You can answer this question without re-solving the model by noticing that we are not meeting the demand for discount fares from JFK to DFW at all. The demand could increase by 100, and we still would not offer more than 11 discount fares.

Alternatively, you could change the demand for discount fares, and re-solve the model. The solution does not change, regardless of how much you increase the demand.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;Yes. American Airlines should market the regular fares from JFK to LAX to increase demand by 50.&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Yes. American Airlines should market the regular fares from JFK to LAX to increase demand by 10.&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;No. American Airlines should not market the regular fares from JFK to LAX because even though the revenue increases, it does not exceed the costs.&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;No. American Airlines should not market the regular fares from JFK to LAX because the revenue does not increase at all by increasing the demand for these tickets.&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

In the current solution, we are meeting the demand for regular tickets from JFK to LAX. If we increase the demand by 10, we offer 10 more regular tickets, but our revenue only increases by $140, which does not exceed the cost of $2000. If we increase the demand by 50, to 130, we only offer 91 seats. Therefore, American Airlines should not market the regular fares from JFK to LAX because even though the revenue increases, it does not exceed the costs.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

*   {{< resource_link 80f150bc-38fd-0f84-75f7-ccfe876f7744 "BackVideo 7: Connecting Flights" >}}
*   {{< resource_link 0cd767eb-f8c6-279f-86f2-16e785139b90 "ContinueVideo 8: The Edge of Revenue Management" >}}