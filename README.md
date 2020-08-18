# Project 2 - Ames Housing Data and Kaggle Challenge

## Problem Statement

This project consists of a Multi-Linear Regression model, trained to predict the expected sale price of a house in Ames, IA based on known characteristics of the unit. Using a dataset from Kaggle.com, we sought to address the following question:

Ideally, using the data available we would like to be able to generalise this model across other cities and still be able to predict with a lower variance from actual data. In reality, we would expect there to be a drop in performance when we attempt to utilise the model created specificially from Ames Housing Data for another city. This in consequence will result in the requirement of additional data from each individual city in question if we want to attempt to achieve generalise for housing data across the USA. Hence, we would rather narrow our scope to at least be able to get a small glimspe on what property features are most important in accurately predicting sale prices of units in Ames, IA? We would also attempt to answer the question of what modeling approach yields the most accurate sale price predictions?

## Executive Summary

In Project 2, we worked with Kaggle data on building sales in Ames, IA that occurred during 2006-2010 to better understand the factors influencing sale prices. We used this understanding to optimize linear regression models, which we then used to make value predictions on Kaggle's test data. We optimized to return the minimum Root Mean Squared Error (RMSE), which Kaggle calculates.

Through the modeling process, we identified a number of key factors and useful methods to build a high-accuracy linear regression model that may be use to predict housing prices for users searching in Ames.

## Data Dictionary

The Data Dictionary has already been linked in courtesy of Dean De Cock of Truman State University [data description](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).

## Conclusions & Recommendations

**Top 10 Feature Correlation**
1. Overall Quality 				(0.80)
2. Exterior Quality				(0.72)
3. Above-Grade Living Area  	(0.72)
4. Kitchen Quality				(0.69)
5. Total Basement Square Ft		(0.67)
6. Garage Area					(0.66)
7. Garage Cars Capacity 		(0.65)
8. First Floor Square Ft		(0.65)
9. Basement Quality				(0.61)
10. Year Built			        (0.57)

**Final Model Details**
 - Regularization: Lasso
 - Scaling: Standard Scalar
 - Cross-Validation R<sup>2</sup> Score: 0.9258
 - R<sup>2</sup> Score on Test Prediction: 0.9021
 - RSME: 24203.23

After going through Linear Regularization, Lasso Regression and Ridge Regressions. The lasso model was eventually chosen due to lower root mean square error as well as higher R<sup>2</sup> score on the test prediction.

**Top 10 Model Coefficients**
1. Above Grade Living Area (24832.4)
2. Overall Quality (12109.9)
3. Type 1 Basement Area (9263.1)
4. Year Built (7888.58)
5. Northridge Heights Neighborhood (7302.22)
6. Total Basement Area (6556.78)
7. Masonry Veneer Area (5861.95)
8. Stonebrook Neighborhood (5698.48)
9. Exertnal Quality (5374.09)
10. Overall Condition (4879.82)

We can see that the major contributing features will be Area followed by quality of the house in question and next will be the neighborhood. The grouping of these factors are the minimum require to produce a model which is capable of doing a prediction that is fairly accurate.

**Recommendations**

For Homeowners who are looking to sell some areas of improvement that they can focus on are the quality/condition of the home before sales they can attempt to artitrage the remodel to increase in sales difference to sell the house for a higher profit.

This model serves as a starting point to model similar cities. It also gives us a close look into the groups of factors that we likely would like to take note if we were to generate a new model for another cities. Additional research should also be done into how to more accurate quantify material categories. Additional features can also be include like crime rate, type of ownership (renters or owners) and more demographics of the neighbhorhood in general.

## Data Sources

Northridge Heights Google Map: https://www.google.com/maps/place/Northridge+Heights+Park/@42.055346,-93.6475705,15.75z/data=!4m5!3m4!1s0x87ee70d870002e1d:0xb084c9e6100e56f2!8m2!3d42.0597732!4d-93.6494713
Northridge Height Satellite Map: https://www.google.com/maps/place/Northridge+Heights+Park/@42.0592842,-93.6495254,3a,75y,214.69h,82.19tdata=!3m6!1e1!3m4!1s5f9pVAST0RW9Mg4IMw0M8A!2e0!7i16384!8i8192!4m5!3m4!1s0x87ee70d870002e1d:0xb084c9e6100e56f2!8m2!3d42.0597732!4d-93.6494713   
Northridge Height Data: https://www.addressreport.com/report/neighborhood/ames-ia/northridge-heights-ames-ia/?display=true        