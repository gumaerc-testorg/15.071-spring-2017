---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '7.3 The Analytical Policeman: Visualization for Law and Order'
parent_type: CourseSection
parent_uid: 716f78f6-1fe6-c5f4-7370-d7a3c4127827
title: '7.3 The Analytical Policeman: Visualization for Law and Order'
uid: 6bc1ec1e-1262-c5a1-28e1-f822404bb0ba
video_metadata:
  youtube_id: null
---
## Quick Question

In this quick question, we'll ask you questions about the following plots. Plot (1) is the heat map we generated at the end of Video 4. Plot (2) and Plot (3) were generated by changing argument values of the command used to generate Plot (1).

**Plot (1)**

{{< resource uuid="bed89f26-4440-1401-1197-fb58867992c7" >}}

**Plot (2)**

{{< resource uuid="be57802c-07c0-cabb-ef69-146663aaec19" >}}

**Plot (3)**

{{< resource uuid="1d25eaf4-f014-1088-66b6-b4a661b87ed1" >}}

Which argument(s) did we change to get Plot (2)? Select all that apply.

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="true" >}} x {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} y {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} fill {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} name {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} low {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} high {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

To get Plot (2), we changed the arguments "x" and "y" (we flipped them). Plot (2) can be generated with the following code:

ggplot(DayHourCounts, aes(x = Var1, y = Hour)) + geom\_tile(aes(fill=Freq)) + scale\_fill\_gradient(name="Total MV Thefts", low="white", high="red") + theme(axis.title.y=element\_blank()){{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

Which argument(s) did we change to get Plot (3)? Select all that apply.

{{< quiz_multiple_choice questionId="Q2_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}} x {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} y {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} fill {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} name {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="false" >}} low {{< /quiz_choice >}}  
{{< quiz_choice isCorrect="true" >}} high {{< /quiz_choice >}}{{< /quiz_choices >}}  
{{< quiz_solution >}}Explanation

To get Plot (3), we changed the argument "high" to "black". Plot (3) can be generated with the following code:

ggplot(DayHourCounts, aes(x = Hour, y = Var1)) + geom\_tile(aes(fill=Freq)) + scale\_fill\_gradient(name="Total MV Thefts", low="white", high="black") + theme(axis.title.y=element\_blank()){{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

- {{% resource_link "7a8ce8b6-91e9-92d1-00a8-3e4b86041a1a" "Back: Video 4: A Heatmap" %}}
- {{% resource_link "0d6e8df1-18b9-6fff-96f8-bda53ace64b7" "Continue: Video 5: A Geographical Hot Spot Map" %}}