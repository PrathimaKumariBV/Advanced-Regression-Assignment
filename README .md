# Advanced Regression Assignment

A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price.

The company is looking at prospective properties to buy to enter the market.

The company wants to know:

* Which variables are significant in predicting the price of a house, and
* How well those variables describe the price of a house.

## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
### Business Goal
Build a model to predict the price of houses with the available independent variables.This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.

### Objective of the Project:
Build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.
Also, determine the optimal value of lambda for ridge and lasso regression.

### Data Description

Based on various meteorological surveys, the firm has gathered a large dataset of housing property details of Australia.

### Feature Description
    Featur description is available in the data dictionary

### Objective of the Assignment
* Build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.
* Also, determine the optimal value of lambda for ridge and lasso regression.
* Find the variables which are significant in predicting the price of a house, and
* Find,how well those variables describe the price of a house.

### 3. Data understanding
#### 3.1 Initial Data Understanding
#### 3.2 Understanding Data set using Dictionary
#### 3.3 Features Description

### 4. EDA
#### 4.1  Univariate Analysis
#### 4.1.1 Univariate Analysis for Numerical variables 
##### disttplot,box plot, value_counts
#### 4.1.2 Descriptive quantile Statistical Analysis
#### 4.2 Bivariate Analysis
#### 4.2.1 Bivariate Analysis for Numerical variables
##### scatter plot,pairplot, heatmap
#### 4.4 Univariate and Bivariate Analysis for Ccategorical Variables
##### bar plot,count plot, value_counts
#### 4.5 Conclusion

### 5. Data Cleaning
     Handling missing values, data imputation ,outlier treatments,creating new derived variables
#### 5.1 Data Imputation
#### 5.2 Map the numerical values of categorical variables to the associated labels
#### 5.3 Create new derived variables
#### 5.4 Outlier Treatment
#### 5.5 Drop some of the features which will not help for our analysis

### 6. Data Preparation
#### 6.1. Create Dummy variables for all the categorical variables
#### 6.2. Divide the data into training and testing data
#### 6.3. Perform Scaling 
#### 6.4. Divide data into dependent and indipendent variables

### 7. Model Building and Evaluation
#### 7.1 Model 1: Included all the independent variables  
##### Evaluate the model by R2-Score ,RSS ,MSE metrics
#### 7.2 Building Models using 'RFE' method 
#### 7.2.1 Model 2: (Build the Linear Regression model by considering top 30 features)
##### Evaluate the model by R2-Score ,RSS ,MSE metrics
##### Evaluate the model by visualizing the patterns of Error term,Error term normality check and visualizing actual and predicted target variable. 
#### 7.2.2 Model 3: (Build the Ridge Regression model by considering top 30 features)
##### Evaluate the model by R2-Score ,RSS ,MSE metrics
##### Evaluate the model Residual Analysis. 
#### 7.2.3 Model 4 : (Build the Lasso Regression model by considering top 10 features)
##### Evaluate the model by R2-Score ,RSS ,MSE metrics
##### Evaluate the model Residual Analysis. 
#### 7.3 Model 5: Build the Ridge Regression model by considering all the features
##### Evaluate the model by R2-Score ,RSS ,MSE metrics
##### Evaluate the model Residual Analysis. 
#### 7.4 Model 6: Build the Lasso Regression model by considering all the features
##### Evaluate the model by R2-Score ,RSS ,MSE metrics
##### Evaluate the model Residual Analysis.  

    - 
## Conclusions

By considering top 30 significant variable selected by RFE method:

    * The Linear regression model with top 30 features gives 91.08% accuracy for training set and 86.05% accuracy for test set. This model is not so bad.
    * Ridge Regression model with top 30 features gives 90.97% accuracy for training set and 86.85% of accuracy for test set.

    * Lasso Regression model with top 30 features gives 90.82% accuracy for training set and 86.05% of accuracy for test set.

By considering all the 273 independent variables while building the model:

    * Ridge Regression is giving model with 94.42% accuracy for training set and 87.79% of accuracy fro the test set.

    *After double the value of alpha (hyper parameter) to build the model using Ridge regression we got 93.87% of accuracy for training set and 86.85% for test set.

    *Lasso Regression is giving model with 94.21% accuracy for training set and 87.86% of accuracy for the test set.

    *After double the value of alpha (hyper parameter) to build the model using Lasso regression we got 93.63% of accuracy for the training set and 87.22% of accuracy for the test set.
    
    # The top significant predictors :
 
 The important predictor variables which helps in predicting the SalePrice of property are as follows:
    
   1. GrLivArea - Above grade (ground) living area square feet
   2. OverallQual_Excellent - Rates the overall material and finish of the house -Excellent. 
   3. AgeOfHouse - Age of the house , we derived this variable by using Year of built and Year of Sold. 
   4.'BsmtFinSF1' - Type 1 finished square feet. If the basement area has high rating and large the price of the property will 
    increases.
   5. 'TotalBsmtSF' -Total square feet of basement area
   6. '1stFlrSF' - 1stFlrSF: First Floor square feet. If the house has large are in first floor the SalePrice will increases.
   7. ExterQual_TA -Evaluates the quality of the material on the exterior - Avarage or Typical. 
   8. GarageArea - Size of garage in square feet. Garage area is positively impacting the SalePrice. If the garage area is 
    large the SalePrice also high.
   9. ExterQual_Fa - Evaluates the quality of the material on the exterior - Fair
   10.OverallQual_Very Good - Rates the overall material and finish of the house - Good
   11. BsmtExposure_Gd -Refers to walkout or garden level walls.
   12. Neighborhood_Crawfor - Physical locations within Ames city limits - Crawford 
   13. ExterQual_Gd - Evaluates the quality of the material on the exterior - Good                 
   14. OverallQual_Very Excellent     
   15. LotArea - Lot size in square feet

  
   1. The Ground living area,Basement finished area,Total basement area,Area of the first floor,Garage area,Lot Area are the 
      important predictors positively impacting the price of the property. 
   2. OverallQuality of the house - If the rating of Overall Quality, material and finish of the house is excellent,good 
      then the price of the property will increases.If it is below average it is negatively impacting the price of the 
      property.
   3. Age of the house,The age of the house is negatively impacting the SalePrice. 
   4. If the quality of the material used on the exterior is Poor , average of typical this will negatively impact the Sale 
      price of the property. 
   5. If the property has walkout or garden level walls this will increases the price of the property.
   6. If the property is near Crawford and NorthRidge then it has high price.
    

## Technologies Used

- Jupyter Notbook (anaconda3)
- Python Language
- pandas library 1.4.1
- numpy library 1.22.2
- seaborn library 0.11.2
- matplotlib library 3.5.1
- sklearn library 0.23.2


## Acknowledgements
Thanks for Upgrad to give this assignment to learn. This is very inspiring assignement to learn many tools and techniques to analyze the data and draw the insights and build different models.

## Contact


Created by,
  -Prathima Kumari B V
  
Developed as part of the  Advanced Regression module required for Advanced Certificate Program for ML and AI - IIIT,Bangalore.