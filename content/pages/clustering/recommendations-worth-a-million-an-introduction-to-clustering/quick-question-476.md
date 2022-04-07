---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '6.2 Recommendations Worth a Million: An Introduction to Clustering '
parent_type: CourseSection
parent_uid: b091b1be-c85a-85e0-60a8-3b7905c9dcce
title: '6.2 Recommendations Worth a Million: An Introduction to Clustering '
uid: 4d3cfab6-9136-623b-888a-5451d2fad159
---

*   {{< resource_link c0ef063d-c722-b998-a530-922a135bd19e "\<Video 7: Hierarchical Clustering in R" >}}
*   {{< resource_link b091b1be-c85a-85e0-60a8-3b7905c9dcce "6.2.1Video 1: Introduction to Netflix" >}}
*   {{< resource_link 0929460c-b5ed-43df-db0e-cacb845ffa3f "6.2.2Quick Question" >}}
*   {{< resource_link ddc4091d-7aa5-1a47-edbc-199cc93c3fb8 "6.2.3Video 2: Recommendation Systems" >}}
*   {{< resource_link 8f7d9b63-f06b-e06b-22b4-9df8cb1010ed "6.2.4Quick Question" >}}
*   {{< resource_link 68624ffa-d0f7-a8c0-1f23-c4a6a20422bb "6.2.5Video 3: Movie Data and Clustering" >}}
*   {{< resource_link b7314818-ce6b-5cbc-b1a5-e7bedcb314f0 "6.2.6Quick Question" >}}
*   {{< resource_link a5ab6699-3ed8-0a0f-758b-18debb6e10a5 "6.2.7Video 4: Computing Distances" >}}
*   {{< resource_link 066f79dd-b024-9424-3545-0a95a9fc60d8 "6.2.8Quick Question" >}}
*   {{< resource_link 9b460c89-6936-6054-88ea-504e144b78ff "6.2.9Video 5: Hierarchical Clustering" >}}
*   {{< resource_link 2f132e05-7445-9a6a-8530-4dc1f0cd7c5c "6.2.10Quick Question" >}}
*   {{< resource_link 97456de3-0891-98f1-c51a-a74e3d11930c "6.2.11Video 6: Getting the Data" >}}
*   {{< resource_link 47a1cfac-748d-6647-732e-f8b91e90cc4f "6.2.12Quick Question" >}}
*   {{< resource_link c0ef063d-c722-b998-a530-922a135bd19e "6.2.13Video 7: Hierarchical Clustering in R" >}}
*   {{< resource_link 4d3cfab6-9136-623b-888a-5451d2fad159 "6.2.14Quick Question" >}}
*   {{< resource_link 9e0e5a25-71bb-afda-ded1-01bdcdce7158 "6.2.15Video 8: The Analytics Edge of Recommendation Systems" >}}
*   {{< resource_link 9e0e5a25-71bb-afda-ded1-01bdcdce7158 "\>Video 8: The Analytics Edge of Recommendation Systems" >}}

Quick Question
--------------

{{< quiz_multiple_choice questionId="Q1_div" >}}{{< quiz_choices >}}{{< quiz_choice isCorrect="false" >}}&nbsp;Action&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Adventure&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Animation&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Children's&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Comedy&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Crime&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Documentary&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="true" >}}&nbsp;Drama&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Fantasy&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Film Noir&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Horror&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Musical&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Mystery&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Romance&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Sci-Fi&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Thriller&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;War&nbsp;{{< /quiz_choice >}}
{{< quiz_choice isCorrect="false" >}}&nbsp;Western&nbsp;{{< /quiz_choice >}}{{< /quiz_choices >}}
{{< quiz_solution >}}Explanation

You can redo the cluster grouping with just two clusters by running the following command:

clusterGroups = cutree(clusterMovies, k = 2)

Then, by using the tapply function just like we did in the video, you can see the average value in each genre and cluster. It turns out that all of the movies in the second cluster belong to the drama genre.

Alternatively, you can use colMeans or lapply as explained below Video 7.{{< /quiz_solution >}}{{< /quiz_multiple_choice >}}

*   {{< resource_link c0ef063d-c722-b998-a530-922a135bd19e "BackVideo 7: Hierarchical Clustering in R" >}}
*   {{< resource_link 9e0e5a25-71bb-afda-ded1-01bdcdce7158 "ContinueVideo 8: The Analytics Edge of Recommendation Systems" >}}