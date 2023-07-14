# Predictive Modeling Analysis of the Lending Club Dataset

This repository shows the steps taken to perform an in-depth analysis of the "[Lending Club Dataset](https://www.lendingclub.com/)" published on the company's website.  

The data and the R Markdown Notebook have been added to the repo so that anyone can recreate the steps involved and add their own insights. 

## Use of:
* **RStudio** version 3.9.7
    * **Main Packages used:** ggplot2, dplyr, tidyr, bestglm, pROC, randomForest
* [**R Markdown**](https://rmarkdown.rstudio.com/)

# Overview
## Key Findings
* Significant predictors with *negative associations* include **term, interest rate, the ratio of monthly debt obligations to self reported income (DTI), revolving line utilization rates,** 
**the number of credit inquiries in the past 6 months, the number of credit inquiries in the past 6 months, the number of derogatory public records, and the**
**number of bankruptcies**
* Significant predictors with *positive associations* include **annual income**

### Model Performance
* Final model chosen: **Relaxed LASSO model corresponding to lambda = lambda first** 
* Model validation misclassifcation rate: **0.283**
* Model validation AUC: **0.6893**
![alt text](https://github.com/monacosc1/lending_club_analysis/blob/master/images/auc.png)

## Exploratory Data Analysis
### Target Variable
* Loan Status
![alt text](https://github.com/monacosc1/lending_club_analysis/blob/master/images/loan_status.png)

### Predictor Variables
* Predictor Variables
![alt text](https://github.com/monacosc1/lending_club_analysis/blob/master/images/predictor_variables.png)


## Main Steps
### Data Cleaning & Exploration
* Conducted an exploratory data analysis to be able to better understand the data and clean it for future forecasting 
* Handled missing data, skewed data, and highly correlated data

### Model Building
* Split data into training, testing, and validation data sets
* Explored different tree-based models and fine-tuned hyperparameters on the best peforming models using 3-fold cross validation with time series split
* Visualized feature importance using Random Forest

### Model Evaluation & Selection
* Evaluated models based on misclassification rates (MCE), area under the curve (AUC), and model interpretability 