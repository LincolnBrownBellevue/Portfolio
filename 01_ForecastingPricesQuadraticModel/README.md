# Time-Series Analysis
# Lincoln Brown

## Overview
This project explores time-series analysis by modeling daily prices using linear and quadratic regression. 
The dataset was developed by Zachary M. Jones, who studies the black market for cannabis in the US. 
The dataset is composed of information pertaining to marijuana where users report the price, quantity, quality, and location of cannabis transactions. 
The goal is to analyze the variability in prices over time, generate predictions, and test for serial correlation in the data and model residuals. 
The analysis leverages statistical and visualization tools to assess model performance and interpret results. 

## Exercise 12-1

We being by importing the file 'mj-clean.csv.' 

Following that, the following functions are defined: 
<ul>
  <li>GroupByDay - Groups transactions by day and computes the daily mean ppg.</li>
  <li>GroupByQualityAndDay - Divides transactions by quality and computes mean daily price.</li>
  <li>PlotFittedValues - Plots original data and fitted values. </li>
  <li>RunLinearModel - Fits a simple linear model</li>
  <li>QuadraticModel - Adds a quadratic term to improve flexibility.</li>
  <li>SimluateResults - Resmaples residuals to simulate results and generate predictions.</li>
  <li>GeneratePredictions - Creates predictions with optional residual noise.</li>
  <li>PlotPredictions - Plots predictions with sampling and residual errors.</li>
</ul>

## Modeling

The Quadratic model is used to accommodate nonlinear qualities of price fluctuations. 

## Interpretation

The model showed a 1% improvement, meaning that the model uses time as an explanatory variable to account for 45% of the observed variability in price. 
These results are also visible in the graph. 

## Prediction

The sampling error (dark gray region) grows larger, but the prediction error (lighter gray) stays about the same. 
The sampling error has more variation towards higher prices, this is due to the nature of a positive quadratic parameter, 
because as it nears the bottom of the parabola, it will meet more resistance and will not be able to continue a downward trend as it would without a quadratic price paramter. 
Essentially, the model is explaining that with the limitations of the sample data, there is less certainty about a decline in the price once it approaches ~$11 per gram.

## Exercise 12-2

Exercise 12-2 tests serial correlation in the raw price data, as well as residuals from the linear and quadratic models. 

## Results

The correlation between consecutive prices has a test statistic of .48 and a pvalue of 0, indicating that it does have a significnat correlation. 


