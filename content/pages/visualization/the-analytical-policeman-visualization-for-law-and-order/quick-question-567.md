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
uid: 28e5e867-d944-5ea9-aa7c-76de722fcf45
video_metadata:
  youtube_id: null
---
## Quick Question

 

In the previous video, our heatmap was plotting squares out in the water, which seems a little strange. We can fix this by removing the observations from our data frame that have Freq = 0.

Take a subset of LatLonCounts, only keeping the observations for which Freq > 0, and call it LatLonCounts2.

Redo the heatmap from the end of Video 5, using LatLonCounts2 instead of LatLonCounts. You should no longer see any squares out in the water, or in any areas where there were no motor vehicle thefts.

How many observations did we remove?

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

You can take a subset of LatLonCounts, only keeping the observations for which Freq > 0 with the following command:

LatLonCounts2 = subset(LatLonCounts, Freq > 0)

Then, you can generate the new heatmap with the following command:

ggmap(chicago) + geom\_tile(data=LatLonCounts2, aes(x = Long, y = Lat, alpha=Freq), fill="red")

The number of observations in LatLonCounts2 is 686, and the number of observations in LatLonCounts is 1638. These numbers can be found by using nrow or str.

CheckShow Answer

 

- [Back: Video 5: A Geographical Hot Spot Map](./resolveuid/0d6e8df118b96fff96f8bda53ace64b7)
- [Continue: Video 6: A Heatmap on the United States](./resolveuid/50eab6cd164e035d9470dc118924f686)