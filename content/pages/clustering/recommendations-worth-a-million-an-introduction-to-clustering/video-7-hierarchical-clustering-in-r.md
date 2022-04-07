---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '6.2 Recommendations Worth a Million: An Introduction to Clustering '
parent_type: CourseSection
parent_uid: b091b1be-c85a-85e0-60a8-3b7905c9dcce
title: '6.2 Recommendations Worth a Million: An Introduction to Clustering '
uid: c0ef063d-c722-b998-a530-922a135bd19e
---

*   {{< resource_link 47a1cfac-748d-6647-732e-f8b91e90cc4f "\<Quick Question" >}}
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
*   {{< resource_link 4d3cfab6-9136-623b-888a-5451d2fad159 "\>Quick Question" >}}

Video 7: Hierarchical Clustering in R
-------------------------------------

**Important Note:** In this video, we use the "ward" method to do hierarchical clustering. This method was recently renamed in R to "ward.D". If you are following along in R while watching the video, you will need to use the following command when doing the hierarchical clustering ("ward" is replaced with "ward.D"):

clusterMovies = hclust(distances, method = "ward.D")

{{< resource 586e592d-afc4-55b0-19b2-7dd6d67ab5bb >}}

An Advanced Approach to Finding Cluster Centroids
-------------------------------------------------

In this video, we explain how you can find the cluster centroids by using the function "tapply" for each variable in the dataset. While this approach works and is familiar to us, it can be a little tedious when there are a lot of variables. An alternative approach is to use the colMeans function. With this approach, you only have one command for each cluster instead of one command for each variable. If you run the following command in your R console, you can get all of the column (variable) means for cluster 1:

colMeans(subset(movies\[2:20\], clusterGroups == 1))

You can repeat this for each cluster by changing the clusterGroups number. However, if you also have a lot of clusters, this approach is not that much more efficient than just using the tapply function.

A more advanced approach uses the "split" and "lapply" functions. The following command will split the data into subsets based on the clusters:

spl = split(movies\[2:20\], clusterGroups)

Then you can use spl to access the different clusters, because

spl\[\[1\]\]

is the same as

subset(movies\[2:20\], clusterGroups == 1)

so colMeans(spl\[\[1\]\]) will output the centroid of cluster 1. But an even easier approach uses the lapply function. The following command will output the cluster centroids for all clusters:

lapply(spl, colMeans)

The lapply function runs the second argument (colMeans) on each element of the first argument (each cluster subset in spl). So instead of using 19 tapply commands, or 10 colMeans commands, we can output our centroids with just two commands: one to define spl, and then the lapply command.

Note that if you have a variable called "split" in your current R session, you will need to remove it with rm(split) so that you can use the split function.

In this video, we use the spreadsheet {{< resource_link f5d06b43-b7c6-dffc-2755-2d12924b69ee "ClusterMeans (ODS" >}}). This file can be opened in LibreOffice or OpenOffice. 

*   {{< resource_link 47a1cfac-748d-6647-732e-f8b91e90cc4f "BackQuick Question" >}}
*   {{< resource_link 4d3cfab6-9136-623b-888a-5451d2fad159 "ContinueQuick Question" >}}