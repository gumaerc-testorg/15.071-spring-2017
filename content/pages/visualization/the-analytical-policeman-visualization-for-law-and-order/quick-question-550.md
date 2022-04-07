---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '7.3 The Analytical Policeman: Visualization for Law and Order'
parent_type: CourseSection
parent_uid: 716f78f6-1fe6-c5f4-7370-d7a3c4127827
title: '7.3 The Analytical Policeman: Visualization for Law and Order'
uid: e685ba71-8462-a41f-dc85-159d8c6cd469
---

*   {{< resource_link 1bd0d7e9-c5ce-0101-823b-0faa796ad873 "\<Video 3: A Line Plot" >}}
*   {{< resource_link 716f78f6-1fe6-c5f4-7370-d7a3c4127827 "7.3.1Video 1: Predictive Policing" >}}
*   {{< resource_link 55ef385f-4486-a0de-2d07-4daf0049a5ab "7.3.2Quick Question" >}}
*   {{< resource_link 647a1b5c-5d6b-626d-39aa-4ad77903806e "7.3.3Video 2: Visualizing Crime Over Time" >}}
*   {{< resource_link 78d60ff4-2d95-ea11-a422-1370f6265996 "7.3.4Quick Question" >}}
*   {{< resource_link 1bd0d7e9-c5ce-0101-823b-0faa796ad873 "7.3.5Video 3: A Line Plot" >}}
*   {{< resource_link e685ba71-8462-a41f-dc85-159d8c6cd469 "7.3.6Quick Question" >}}
*   {{< resource_link 7a8ce8b6-91e9-92d1-00a8-3e4b86041a1a "7.3.7Video 4: A Heatmap" >}}
*   {{< resource_link 6bc1ec1e-1262-c5a1-28e1-f822404bb0ba "7.3.8Quick Question" >}}
*   {{< resource_link 0d6e8df1-18b9-6fff-96f8-bda53ace64b7 "7.3.9Video 5: A Geographical Hot Spot Map" >}}
*   {{< resource_link 28e5e867-d944-5ea9-aa7c-76de722fcf45 "7.3.10Quick Question" >}}
*   {{< resource_link 50eab6cd-164e-035d-9470-dc118924f686 "7.3.11Video 6: A Heatmap on the United States" >}}
*   {{< resource_link 578178b9-992b-b5c4-e6a9-8dc2f7c1ad78 "7.3.12Quick Question" >}}
*   {{< resource_link d2e3fa0c-b97e-d8cd-0b39-1b4b43303794 "7.3.13Video 7: The Analytics Edge" >}}
*   {{< resource_link 7a8ce8b6-91e9-92d1-00a8-3e4b86041a1a "\>Video 4: A Heatmap" >}}

Quick Question
--------------

Create a new line plot, like the one in Video 3, but add the argument "linetype=2". So the geom\_line part of the plotting command should look like:

geom\_line(aes(group=1), linetype=2)

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;Makes the line thicker&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Changes the color of the line to blue&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;Makes the line dashed&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Makes the line lighter in color&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

The linetype parameter makes the line dashed, and the alpha parameter makes the line lighter in color, or more transparent. The two plots can be generated with the following commands:

ggplot(WeekdayCounts, aes(x = Var1, y = Freq)) + geom\_line(aes(group=1), linetype=2) + xlab("Day of the Week") + ylab("Total Motor Vehicle Thefts")

ggplot(WeekdayCounts, aes(x = Var1, y = Freq)) + geom\_line(aes(group=1), alpha=0.3) + xlab("Day of the Week") + ylab("Total Motor Vehicle Thefts"){{< /quiz_solution >}}{{< /quiz_multiple_choice >}}{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;Makes the line thicker&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Changes the color of the line to blue&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Makes the line dashed&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;Makes the line lighter in color&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

The linetype parameter makes the line dashed, and the alpha parameter makes the line lighter in color, or more transparent. The two plots can be generated with the following commands:

ggplot(WeekdayCounts, aes(x = Var1, y = Freq)) + geom\_line(aes(group=1), linetype=2) + xlab("Day of the Week") + ylab("Total Motor Vehicle Thefts")

ggplot(WeekdayCounts, aes(x = Var1, y = Freq)) + geom\_line(aes(group=1), alpha=0.3) + xlab("Day of the Week") + ylab("Total Motor Vehicle Thefts"){{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

*   {{< resource_link 1bd0d7e9-c5ce-0101-823b-0faa796ad873 "BackVideo 3: A Line Plot" >}}
*   {{< resource_link 7a8ce8b6-91e9-92d1-00a8-3e4b86041a1a "ContinueVideo 4: A Heatmap" >}}