---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '7.2 Visualizing the World: An Introduction to Visualization'
parent_type: CourseSection
parent_uid: 274ac6b9-daf6-cd65-874e-c643ab327953
title: '7.2 Visualizing the World: An Introduction to Visualization'
uid: a7c29773-2c9a-e308-c35b-598232cd91c6
---

*   {{< resource_link be1c12bd-caf2-9b71-c12f-50c42551b8a6 "\<Video 5: Advanced Scatterplots Using ggplot" >}}
*   {{< resource_link 274ac6b9-daf6-cd65-874e-c643ab327953 "7.2.1Video 1: The Power of Visualizations" >}}
*   {{< resource_link dc9db678-f128-3a5e-3783-460ede434049 "7.2.2Quick Question" >}}
*   {{< resource_link c0e12457-eea5-7533-f2df-4a7f420a5b38 "7.2.3Video 2: The World Health Organization (WHO)" >}}
*   {{< resource_link ad37df74-c536-e3bf-54d8-546ea7d3b482 "7.2.4Quick Question" >}}
*   {{< resource_link c8e9fd0f-cbd8-682c-ff60-a63c2596b948 "7.2.5Video 3: What is Data Visualization?" >}}
*   {{< resource_link afc1a35a-1de0-dfbe-71d4-6f725359bcfc "7.2.6Quick Question" >}}
*   {{< resource_link bcd276c5-4387-e04d-4149-dfe97b763b3f "7.2.7Video 4: Basic Scatterplots Using ggplot" >}}
*   {{< resource_link 9df5bf16-9354-da79-32a2-7538c025bb7e "7.2.8Quick Question" >}}
*   {{< resource_link be1c12bd-caf2-9b71-c12f-50c42551b8a6 "7.2.9Video 5: Advanced Scatterplots Using ggplot" >}}
*   {{< resource_link a7c29773-2c9a-e308-c35b-598232cd91c6 "7.2.10Quick Question" >}}
*   {{< resource_link 716f78f6-1fe6-c5f4-7370-d7a3c4127827 "\>The Analytical Policeman: Visualization for Law and Order" >}}

Quick Question
--------------

Create the fertility rate versus population under 15 plot again:

ggplot(WHO, aes(x = FertilityRate, y = Under15)) + geom\_point()

Now, color the points by the Region variable.

Note: You can add scale\_color\_brewer(palette="Dark2") to your plot if you are having a hard time distinguishing the colors (this color palette is often better if you are colorblind). To use this option, you should just add scale\_color\_brewer(palette="Dark2") to your plotting command right after geom\_point().

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;Africa&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Americas&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Eastern Mediterranean&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;Europe&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;South-East Asia&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Western Pacific&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

You can color the points by region if you adjust the command to the following:

ggplot(WHO, aes(x = FertilityRate, y = Under15, color=Region)) + geom\_point()

Most of the countries in Europe have a very low fertility rate and a very low percentage of the population under 15.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

*   {{< resource_link be1c12bd-caf2-9b71-c12f-50c42551b8a6 "BackVideo 5: Advanced Scatterplots Using ggplot" >}}
*   {{< resource_link 716f78f6-1fe6-c5f4-7370-d7a3c4127827 "ContinueThe Analytical Policeman: Visualization for Law and Order" >}}