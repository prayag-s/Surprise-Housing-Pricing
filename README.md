# Surprise-Housing-Pricing

   <p align="right">By Prayag Sanjay</p>

## Problem Statement
  US based firm Surpise Housing is looking to enter Australian market.
  Their aim is to buy properties at low prices and then sell them at higher prices.

  They have collected an extensive data of propety prices and their features
  and want to find prospective properties which then can buy cheap and then
  sell at maximum profits.

  Hence,

  Goals of Study
  
  1. To find out which variables are significant in predicting properties.

  2. How well those variables describe the price of a property ?

  3. Use Lasso and Ridge regression to build an accurate model.

  Business Goals
  
  1. To build a model to predict the price of the property based on available features.

  2. To explain the dynamics of the pricing and market based on the model to
     identify areas which will yield maximum profit

## Data Set
	We are give a dataset on property prices across Australia and various probable
  factors affecting the price such as area , garage, pools, bedrooms, utilities
  and neighbourhood charactersitcs such as proximity to streets, market etc.

## Approach
	From the problem statement, we can see following characterstics

  Business wants to know the driver variables for a specific target,
  in this house prices. So there is an expectation of **explainability**
  from the model.

  Business want to predict price of house or dynamics of demand as
  opposed to forecast the price of houses.
  Thus this problem falls in realms of predictive analysis where we want to
  interpolate the data. Aa a result of above two reasons we will employ
  Linear Regression with regularisation using Lasso and Ridge Regression
  machine learning methods to build the model which will answer the business questions.
	

## Steps
	-	Perform cleaning of data
	-	Exploratory data analysis of data. Use visualization.
	-	Divide the data in test and training sets.
	-	Do modelling on the training set.
	-	Iterate till variables are statistically coefficient, there is no multicollinearity.
	-	Check the linear regression assumptions on the training data.
	-	Predict using the best model on the test data.
	-	Check that there is no under or over fitting using metrics such adjusted R-square.


## Conclusion

### Variables that are significant in predicting the price of the house.

Following variables are significant

**Lot Area**

**Base Finish (Type 1)**

**Total Basement Area** 

**First Floor Area**

**2nd Floor Area**

**Age of house**

**Overall Condition of House** (in particular if it is Excellent, Very good and Good)

**Overall Quality** (in particular if it is Excellent)

**Exterior Covering on house** (if it is Cement)

### Dynamics of the demand

  Based up on above variables and their coefficients, we can group drivers variables in following groups

  **Positive Drivers**

  These variables increase the price of the house. So company should check and buy properties having these characterstics

  Lot Area

  Base Finish (Type 1)

  Total Basement Area

  First Floor Area

  2nd Floor Area

  Overall Condition of House (in particular if it is Excellent, Very good and Good)

  Exterior Covering on house (if it is Cement and covering is of one type only)

  **Negative Drivers**

  Age of house

  Exterior Covering on house (if it is Cement and covering is more than one type)

### Model to describe the demand (by Lasso)

	The model is

    count = 177574.75 * constant + 8465.27  * LotArea + 10055.42 *  BsmtFinSF1 + 
    11282.11 *es TotalBsmtSF + 16236.42 * 1stFlrSF + 22601.86 * 2ndFlrSF 
    - 13339.15 * AgeHouse + 9718.89 * OverallQual_Good + 18241.77
    * OverallQual_VeryGood + 18289.10 * OverallQual_Excellent +
    12655.55 * OverallQual_10 + 2886.99 * Exterior1st_CemntB
    - 1923.05 * Exterior2nd_CmentBd	
