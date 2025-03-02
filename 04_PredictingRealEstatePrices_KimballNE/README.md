## Predicting Real Estate Prices in Kimball, NE

## Overview

This project aims to predict the sale price of houses in Kimball, NE using features such as size and location. The data was obtained from the Kimball, NE County Assessor's GIS website. The primary object is to gain a better understading of real estate market conditions. A predictive model using publicly available data provides insights into a house's value, assisting in purchasing or selling decisions. 

Predicting housing sale prices benefits various stakeholders, including homeowners, real estate agents, and potential buyers. Accurate predictions enable informed decision-making regarding fair listing prices, negotiating deals, and identifying economical purchases. 

Data was obtained via an API from Kimball's Assessor's GIS website. Although the website states that the data should not be used for legal documentation, it is accurate enough for this project's purposes. Other counties in the state use similar websites, allowing this approach to be applied elsewhere. 

## Milestone 1: Data Collection and Analysis
## Data Collection 
<ul>
    <li>Pulled data by obtaining a list of Parcel IDs for Kimball, NE and retrieving property details via an API.</li>
    <li>Constructed a dataframe containing relevant features</li>
    <li>Initial dataset 722 records and 12 features</li>
</ul>

## Exploratory Data Analysis (EDA)
<ul>
    <li>Checked for duplicates and analyzed available featurees.</li>
    <li>Examined correlation between features and target variable (sale price)</li>
    <li>Removed outliers and performed feature engineering</li>
</ul>

## Key Findings
<ul>
    <li>Most houses sold for less than $100,000</li>
    <li>assessed_value showed the strongest correlation with sale_price</li>
    <li>total_sqft had a weaker correlation, indicating that Linear Regression might not be the best model</li>
</ul>

## Milestone 2: Feature Engineering and Model Comparison
## Feature Engineering
<ul>
    <li>Created additional features like bed_bath_interaction, year_group, and sale_price_zscore</li>
    <li>Addressed missing values by imputing zeroes for garage_size</li>
    <li>Standardized categorical features like condition and quality by converting them into numerical categories</li>
    <li>Cleaned dataset: 708 records and 16 features</li>
</ul>

## Model Comparison
<ul>
    <li>Evaluated Models: Linear Regression, Decision Tree, and Random Forest</li>
    <li>Applied feature selection techniques such as PCA and ANOVA, which did not improve performance</li>
    <li>Focused on hyperparameter tuning for Decision Tree and Random Forest in Milestone 3</li>

## Milestone 3: Model Tuning and Evaluation
## Baseline Model
<ul>
    <li>Established a baseline using Dummy Regressor</li>
    <li>Decision Tree and Random Forest performed best, warranting further tuning</li>
</ul>

## Hyperparameter Tuning
<ul>
    <li>Used GridSearchCV to optimize Decision Tree and Random Forest models</li>
    <li>Evaluated models using R-Square (R2), Root Mean Squared Error (RMSE), and Mean Absolute Error (MAE)</li>
    <li>Feature importance analysis identified sale_year as the second-most important feature</li>
</ul>

## Model Performance
Compared 8 models:
<ul>
    <li>Baseline (Dummy Regressor)</li>
    <li>Linear Regression</li>
    <li>Linear Regression with PCA</li>
    <li>Linear Regression with ANOVA</li>
    <li>Decision Tree</li>
    <li>Tuned Decision Tree</li>
    <li>Random Forest</li>
    <li>Tuned Random Forest</li>
</ul>
Tuned Random Forest achieved the best results with an MAE of $22,667.12.

## Conclusion 

The Tuned Random Forest model demonstrated the best predicitive performance with an MAE of $22,667.12. While the model is not intended for deployment, it provides valuable insights into housing market trends. 

## Future Improvements
<ol>
    <li>Increase Dataset Size: Adding data from nearby counties could enhance accuracy.</li>
    <li>Explore Geographic Influences: Using neighborhood-level data or street names may uncover hidden trends</li>
    <li>Further Analyze sale_year Impact: Understanding market trends beyond five years could refine predictions</li>
</ol>

The primary limitation is the small dataset size due to the limited number of house sales in Kimball. Instead of using older data, incorporating sales from nearby counties may be a better strategy. 
In summary, the Tuned Random Forest model effectively predicts house sale prices within an acceptable margin of error. However, additional data and feature enhancements could further refine its accuracy, making it a more useful tool for real estate anaylsis. 