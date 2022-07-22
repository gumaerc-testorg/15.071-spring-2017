---
content_type: page
description: ''
draft: false
learning_resource_types: []
ocw_type: CourseSection
parent_title: 2 Linear Regression
parent_type: CourseSection
parent_uid: c846ced6-fc6d-3bc9-64e0-47324e251a98
title: 2.5 Assignment 2
uid: d3823600-300c-0300-0e79-696e835f8f2f
video_metadata:
  youtube_id: null
---
## Climate Change

There have been many studies documenting that the average global temperature has been increasing over the last century. The consequences of a continued rise in global temperature will be dire. Rising sea levels and an increased frequency of extreme weather events will affect billions of people.

In this problem, we will attempt to study the relationship between average global temperature and several other factors.

The file [climate\_change (CSV)](./resolveuid/3b53e75d1ddb97bd98f40ae5bbee2475) contains climate data from May 1983 to December 2008. The available variables include:

 

- *Year*: the observation year.
- *Month*: the observation month.
- *Temp*: the difference in degrees Celsius between the average global temperature in that period and a reference value. This data comes from the [Climatic Research Unit at the University of East Anglia](https://sites.uea.ac.uk/cru/).
- *CO2*, *N2O*, *CH4*, *CFC.11*, *CFC.12*: atmospheric concentrations of carbon dioxide (CO2), nitrous oxide (N2O), methane  (CH4), trichlorofluoromethane (CCl3F; commonly referred to as CFC-11) and dichlorodifluoromethane (CCl2F2; commonly referred to as CFC-12), respectively. This data comes from the [ESRL/NOAA Global Monitoring Division](http://www.esrl.noaa.gov/gmd/ccgg/data-products.html).
- CO2, N2O and CH4 are expressed in ppmv (parts per million by volume  -- i.e., 397 ppmv of CO2 means that CO2 constitutes 397 millionths of the total volume of the atmosphere)
- CFC.11 and CFC.12 are expressed in ppbv (parts per billion by volume). 
- *Aerosols*: the mean stratospheric aerosol optical depth at 550 nm. This variable is linked to volcanoes, as volcanic eruptions result in new particles being added to the atmosphere, which affect how much of the sun's energy is reflected back into space. This data is from the [Godard Institute for Space Studies at NASA](http://data.giss.nasa.gov/modelforce/strataer/).
- *TSI*: the total solar irradiance (TSI) in W/m2 (the rate at which the sun's energy is deposited per unit area). Due to sunspots and other solar phenomena, the amount of energy that is given off by the sun varies substantially with time. This data is from the [SOLARIS-HEPPA project website](http://solarisheppa.geomar.de/solarisheppa/cmip5).  
     
- *MEI*: multivariate El Nino Southern Oscillation index (MEI), a measure of the strength of the [El Nino/La Nina-Southern Oscillation](http://en.wikipedia.org/wiki/El_nino) (a weather effect in the Pacific Ocean that affects global temperatures). This data comes from the [ESRL/NOAA Physical Sciences Division](https://www.esrl.noaa.gov/psd/).

## Problem 1.1 - Creating Our First Model

We are interested in how changes in these variables affect future temperatures, as well as how well these variables explain temperature changes so far. To do this, first read the dataset climate\_change.csv into R.

Then, split the data into a *training set*, consisting of all the observations up to and including 2006, and a *testing set* consisting of the remaining years (hint: use subset). A training set refers to the data that will be used to build the model (this is the data we give to the lm() function), and a testing set refers to the data we will use to test our predictive ability.

Next, build a linear regression model to predict the dependent variable Temp, using MEI, CO2, CH4, N2O, CFC.11, CFC.12, TSI, and Aerosols as independent variables (*Year* and *Month* should NOT be used in the model). Use the training set to build the model.

Enter the model R2 (the "Multiple R-squared" value):

Exercise 1

&nbsp;Numerical Response&nbsp;

 

Explanation

First, read in the data and split it using the subset command:

climate = read.csv("climate\_change.csv")

train = subset(climate, Year \<= 2006)

test = subset(climate, Year > 2006)

Then, you can create the model using the command:

climatelm = lm(Temp ~ MEI + CO2 + CH4 + N2O + CFC.11 + CFC.12 + TSI + Aerosols, data=train)

Lastly, look at the model using summary(climatelm). The Multiple R-squared value is 0.7509.

CheckShow Answer

## Problem 1.2 - Creating Our First Model

Which variables are significant in the model? We will consider a variable signficant only if the p-value is below 0.05. (Select all that apply.)

Exercise 2

&nbsp;MEI&nbsp;

&nbsp;CO2&nbsp;

&nbsp;CH4&nbsp;

&nbsp;N2O&nbsp;

&nbsp;CFC.11&nbsp;

&nbsp;CFC.12&nbsp;

&nbsp;TSI&nbsp;

&nbsp;Aerosols&nbsp;

 

Explanation

If you look at the model we created in the previous problem using summary(climatelm), all of the variables have at least one star except for CH4 and N2O. So MEI, CO2, CFC.11, CFC.12, TSI, and Aerosols are all significant.

CheckShow Answer

## Problem 2.1 - Understanding the Model

Current scientific opinion is that nitrous oxide and CFC-11 are greenhouse gases: gases that are able to trap heat from the sun and contribute to the heating of the Earth. However, the regression coefficients of both the N2O and CFC-11 variables are **negative**, indicating that increasing atmospheric concentrations of either of these two compounds is associated with lower global temperatures.

Which of the following is the *simplest* correct explanation for this contradiction?

Exercise 3

&nbsp;Climate scientists are wrong that N2O and CFC-11 are greenhouse gases - this regression analysis constitutes part of a disproof.&nbsp;

&nbsp;There is not enough data, so the regression coefficients being estimated are not accurate.&nbsp;

&nbsp;All of the gas concentration variables reflect human development - N2O and CFC.11 are correlated with other variables in the data set.&nbsp;

Explanation

The linear correlation of N2O and CFC.11 with other variables in the data set is quite large. The first explanation does not seem correct, as the warming effect of nitrous oxide and CFC-11 are well documented, and our regression analysis is not enough to disprove it. The second explanation is unlikely, as we have estimated eight coefficients and the intercept from 284 observations.

CheckShow Answer

## Problem 2.2 - Understanding the Model

Compute the correlations between all the variables in the training set. Which of the following independent variables is N2O highly correlated with (absolute correlation greater than 0.7)? Select all that apply.

Exercise 4

&nbsp;MEI&nbsp;

&nbsp;CO2&nbsp;

&nbsp;CH4&nbsp;

&nbsp;CFC.11&nbsp;

&nbsp;CFC.12&nbsp;

&nbsp;Aerosols&nbsp;

&nbsp;TSI&nbsp;

 

Which of the following independent variables is CFC.11 highly correlated with? Select all that apply.

Exercise 5

&nbsp;MEI&nbsp;

&nbsp;CO2&nbsp;

&nbsp;CH4&nbsp;

&nbsp;N2O&nbsp;

&nbsp;CFC.12&nbsp;

&nbsp;Aerosols&nbsp;

&nbsp;TSI&nbsp;

 

Explanation

You can calculate all correlations at once using cor(train) where train is the name of the training data set.

CheckShow Answer

## Problem 3 - Simplifying the Model

Given that the correlations are so high, let us focus on the N2O variable and build a model with only MEI, TSI, Aerosols and N2O as independent variables. Remember to use the training set to build the model.

Enter the coefficient of N2O in this reduced model:

Exercise 6

&nbsp;Numerical Response&nbsp;

 

(How does this compare to the coefficient in the previous model with all of the variables?)

Enter the model R2:

Exercise 7

&nbsp;Numerical Response&nbsp;

 

Explanation

We can create this simplified model with the command:

LinReg = lm(Temp ~ MEI + N2O + TSI + Aerosols, data=train)

You can get the coefficient for N2O and the model R-squared by typing summary(LinReg).

We have observed that, for this problem, when we remove many variables the sign of N2O flips. The model has not lost a lot of explanatory power (the model R2 is 0.7261 compared to 0.7509 previously) despite removing many variables. As discussed in lecture, this type of behavior is typical when building a model where many of the independent variables are highly correlated with each other. In this particular problem many of the variables (CO2, CH4, N2O, CFC.11 and CFC.12) are highly correlated, since they are all driven by human industrial development.

CheckShow Answer

- [Back: Video 4: Making Predictions](./resolveuid/4a72056c6bbe0c01489fb7068637be07)
- [Continue: Reading Test Scores](./resolveuid/f590aa024205ae291d855ec56a16b4a4)