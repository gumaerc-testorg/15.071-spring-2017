---
content_type: page
learning_resource_types: []
ocw_type: CourseSection
parent_title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
parent_type: CourseSection
parent_uid: 3063320a-4175-6b8a-4fa9-892f61b52c0d
title: '3.2 Modeling the Expert: An Introduction to Logistic Regression'
uid: 8fc17cbb-03cd-ce23-b588-0c21e7dc33e8
---

*   {{< resource_link 9cb7a258-ad19-0f7f-84e5-89aad47092b1 "\<Quick Question" >}}
*   {{< resource_link 3063320a-4175-6b8a-4fa9-892f61b52c0d "3.2.1Video 1: Replicating Expert Assessment" >}}
*   {{< resource_link a92dcb88-eddd-40ad-72c0-d5bc2288c90e "3.2.2Video 2: Building the Dataset" >}}
*   {{< resource_link 4551bb95-ca82-a0ca-cf08-eda74141daaa "3.2.3Quick Question" >}}
*   {{< resource_link 8099bebb-d4e8-1ce0-9baa-3ede1f3ec357 "3.2.4Video 3: Logistic Regression" >}}
*   {{< resource_link 9cb7a258-ad19-0f7f-84e5-89aad47092b1 "3.2.5Quick Question" >}}
*   {{< resource_link 8fc17cbb-03cd-ce23-b588-0c21e7dc33e8 "3.2.6Video 4: Logistic Regression in R" >}}
*   {{< resource_link 8c080206-9993-5e2b-b0c5-0c4cd73fd74c "3.2.7Quick Question" >}}
*   {{< resource_link 7bf86a6c-2bb6-629e-d20e-4dd216833197 "3.2.8Video 5: Thresholding" >}}
*   {{< resource_link d565e093-b63d-b842-9332-eabcb8503b85 "3.2.9Quick Question" >}}
*   {{< resource_link f6216265-1257-bdbe-4826-8a5e5b311096 "3.2.10Video 6: ROC Curves" >}}
*   {{< resource_link d9817f81-c4ac-257a-ed44-548eaa714059 "3.2.11Quick Question" >}}
*   {{< resource_link 1e61720e-cc15-0a7b-0c5e-b3fe60c5ffa1 "3.2.12Video 7: Interpreting the Model" >}}
*   {{< resource_link 8809159b-6e06-0da2-d386-90c7900fdd67 "3.2.13Quick Question" >}}
*   {{< resource_link 81d5d93d-77c2-b8fc-0b85-d9cbcdc418a5 "3.2.14Video 8: The Analytics Edge" >}}
*   {{< resource_link 8c080206-9993-5e2b-b0c5-0c4cd73fd74c "\>Quick Question" >}}

Video 4: Logistic Regression in R
---------------------------------

In this video, we'll be using the dataset {{< resource_link 6343d35a-6e78-1756-0160-a4ea9dc9bd2e "quality (CSV)" >}} to build a logistic regression model in R. Please download this file to follow along.

An R script file with all of the commands used in this lecture can be downloaded here: {{< resource_link b6bc9877-49db-0911-1285-d5a2a287e733 "Unit3\_ModelingExpert (R)" >}}.

{{< resource d56beae6-5d3e-cccc-adba-697fc8c6288b >}}

The variables in the dataset quality.csv are as follows:

*   **MemberID** numbers the patients from 1 to 131, and is just an identifying number.
*   **InpatientDays** is the number of inpatient visits, or number of days the person spent in the hospital.
*   **ERVisits** is the number of times the patient visited the emergency room.
*   **OfficeVisits** is the number of times the patient visited any doctor's office.
*   **Narcotics** is the number of prescriptions the patient had for narcotics.
*   **DaysSinceLastERVisit** is the number of days between the patient's last emergency room visit and the end of the study period (set to the length of the study period if they never visited the ER). 
*   **Pain** is the number of visits for which the patient complained about pain.
*   **TotalVisits** is the total number of times the patient visited any healthcare provider.
*   **ProviderCount** is the number of providers that served the patient.
*   **MedicalClaims** is the number of days on which the patient had a medical claim.
*   **ClaimLines** is the total number of medical claims.
*   **StartedOnCombination** is whether or not the patient was started on a combination of drugs to treat their diabetes (TRUE or FALSE).
*   **AcuteDrugGapSmall** is the fraction of acute drugs that were refilled quickly after the prescription ran out.
*   **PoorCare** is the outcome or dependent variable, and is equal to 1 if the patient had poor care, and equal to 0 if the patient had good care.

In this video we learned how to use the sample.split() function from the caTools package to split data for a classification problem, balancing the positive and negative observations in the training and testing sets.

If you wanted to instead split a data frame _data,_ where the dependent variable is a continuous outcome (this was the case for all the datasets we used last week), you could instead use the sample() function. Here is how to select 70% of observations for the training set (called "train") and 30% of observations for the testing set (called "test"):

`spl = sample(1:nrow(data), size=0.7 * nrow(data))`

`train = data[spl,]`

`test = data[-spl,]`

*   {{< resource_link 9cb7a258-ad19-0f7f-84e5-89aad47092b1 "BackQuick Question" >}}
*   {{< resource_link 8c080206-9993-5e2b-b0c5-0c4cd73fd74c "ContinueQuick Question" >}}