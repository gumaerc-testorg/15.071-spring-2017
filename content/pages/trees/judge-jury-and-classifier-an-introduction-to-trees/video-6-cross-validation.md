---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '4.2 Judge, Jury, and Classifier: An Introduction to Trees '
parent_type: CourseSection
parent_uid: 11f9b44d-c296-0689-414b-8c313764a18d
title: '4.2 Judge, Jury, and Classifier: An Introduction to Trees '
uid: aed8634b-040d-d1af-7abb-68e999cb9c43
---

*   {{< resource_link ff7dc49d-2cde-fc1a-c3e5-d01f07046ac1 "\<Quick Question" >}}
*   {{< resource_link 11f9b44d-c296-0689-414b-8c313764a18d "4.2.1Video 1: The Supreme Court" >}}
*   {{< resource_link b707db7f-9900-9e83-423e-4911e4d83568 "4.2.2Quick Question" >}}
*   {{< resource_link fbeabfb3-e0a4-b479-efe5-ffb5d7cf5d4a "4.2.3Video 2: CART" >}}
*   {{< resource_link 076a36dd-c951-926f-d5c9-9ccb41e476d9 "4.2.4Quick Question" >}}
*   {{< resource_link ca1564b0-9178-66a3-a00e-801c8c9fdbbc "4.2.5Video 3: Splitting and Predictions" >}}
*   {{< resource_link 9788174f-bc23-8176-2178-73d882264bfd "4.2.6Quick Question" >}}
*   {{< resource_link a0af0b83-fff4-3d63-4dfe-02e15106f92d "4.2.7Video 4: CART in R" >}}
*   {{< resource_link 8f336b6d-3260-d3a1-28f2-88e99dda1c42 "4.2.8Quick Question" >}}
*   {{< resource_link d818f062-0c7e-3cee-9435-07c440503537 "4.2.9Video 5: Random Forests" >}}
*   {{< resource_link ff7dc49d-2cde-fc1a-c3e5-d01f07046ac1 "4.2.10Quick Question" >}}
*   {{< resource_link aed8634b-040d-d1af-7abb-68e999cb9c43 "4.2.11Video 6: Cross-Validation" >}}
*   {{< resource_link 0be06c80-7e39-cc4e-2808-dc63ffaa5efa "4.2.12Quick Question" >}}
*   {{< resource_link 2ca2e4f1-74a6-6019-fbe6-8e97bba87376 "4.2.13Video 7: The Model v. The Experts" >}}
*   {{< resource_link 0be06c80-7e39-cc4e-2808-dc63ffaa5efa "\>Quick Question" >}}

Video 6: Cross-Validation
-------------------------

**Important Note:** In this video, we install and load two new packages so that we can perform cross-validation: "caret", and "e1071". You may need to additionally install and load the following packages for cross-validation to work on your computer: "class" and "ggplot2". If you receive an error message after trying to load caret and e1071, please try installing and loading these two additional packages.

{{< resource 2c3b5765-3e27-972f-2133-56dd1c0025e1 >}}

Cross-Validation for Random Forests
-----------------------------------

You might be wondering why we used cross-validation on our CART model, but not on our random forest model. According to the creaters of the random forest algorithm, the model is not very sensitive to the parameters and therefore does not easily overfit to the training set. You can read more on [the Random Forests website](https://www.stat.berkeley.edu/~breiman/RandomForests/cc_home.htm). 

However, if you are interested in experimenting with the parameters of the random forest model more, you can read about the parameters and cross-validation for random forests in the ![This resource may not render correctly in a screen reader.](/images/inacessible.gif)[documentation for the randomForest package (PDF)](http://cran.r-project.org/web/packages/randomForest/randomForest.pdf).

*   {{< resource_link ff7dc49d-2cde-fc1a-c3e5-d01f07046ac1 "BackQuick Question" >}}
*   {{< resource_link 0be06c80-7e39-cc4e-2808-dc63ffaa5efa "ContinueQuick Question" >}}