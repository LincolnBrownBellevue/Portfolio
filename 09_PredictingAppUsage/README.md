## Predicting App Usage

## Overview
This project aims to provide actionable insights by identifying key factors associated with app usage time. Key analysis will focus on the correlation between features such as screen-on time, daily data consumption, age, gender, operating system, and device model to determine which factors are most important for predicting app usage time. The target feature for the analysis is the ‘App Usage Time (MB/Day)’ feature. There were three models created for this project, a linear regression model, random forest regression model, and an XGBoost regression model.


## Dataset
The dataset used in this project is Mobile Device Usage and User Behavior Dataset found on Kaggle, uploaded by user Vala Khorasani. The dataset contains 700 samples of user data including metrics such as app usage time, screen-on time, battery drain, number of apps installed, data usage, and user specific features such as age and gender. 

## Dependencies
<ul>
    <li>pandas</li>
    <li>matplotlib</li>
    <li>numpy</li>
    <li>scipy</li>
    <li>seaborn</li>
    <li>scikit-learn</li>
    <li>xgboost</li>
</ul>

## Findings
This project aimed to investigate the features that influence app usage time and to determine which predictive model performed the best at predicting app usage time with the dataset Mobile Device Usage and User Behavior and which features were the most important for predicting app usage. Through the comparison of three models Linear Regression, Random Forest, and XGBoost, it was determined that the Random Forest Model had the best predictive performance, with the lowest MAE and RMSE scores and the highest R2 score. The features that were most significant predictors for app usage time were number of apps installed, daily battery drain, and daily data usage. This aligns with expectations, given that these three features directly correlate with how users engage with apps on their device. 
