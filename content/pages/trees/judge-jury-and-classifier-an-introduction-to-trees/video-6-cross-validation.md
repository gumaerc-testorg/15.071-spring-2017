---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: '4.2 Judge, Jury, and Classifier: An Introduction to Trees '
parent_type: CourseSection
parent_uid: 11f9b44d-c296-0689-414b-8c313764a18d
title: '4.2 Judge, Jury, and Classifier: An Introduction to Trees'
uid: aed8634b-040d-d1af-7abb-68e999cb9c43
video_metadata:
  youtube_id: null
---
## Video 6: Cross-Validation

**Important Note:** In this video, we install and load two new packages so that we can perform cross-validation: "caret", and "e1071". You may need to additionally install and load the following packages for cross-validation to work on your computer: "class" and "ggplot2". If you receive an error message after trying to load caret and e1071, please try installing and loading these two additional packages.

{{< resource uuid="2c3b5765-3e27-972f-2133-56dd1c0025e1" >}}

## Cross-Validation for Random Forests

You might be wondering why we used cross-validation on our CART model, but not on our random forest model. According to the creaters of the random forest algorithm, the model is not very sensitive to the parameters and therefore does not easily overfit to the training set. You can read more on {{% resource_link "527a3e1d-7800-4e2f-a803-1858b8b1e351" "the Random Forests website" %}}. 

However, if you are interested in experimenting with the parameters of the random forest model more, you can read about the parameters and cross-validation for random forests in the {{% resource_link "0d7544cc-53b3-4ba0-a0e8-eee6a08fb003" "documentation for the randomForest package (PDF)" %}}.

- {{% resource_link "ff7dc49d-2cde-fc1a-c3e5-d01f07046ac1" "BackQuick Question" %}}
- {{% resource_link "0be06c80-7e39-cc4e-2808-dc63ffaa5efa" "ContinueQuick Question" %}}