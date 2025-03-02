## Detecting Phishing Emails

## Overview
Emails are a popular platform for attackers to gain access to a network. Using phishing emails, malicious actors harvest user credentials which they can then use to gain access to sensitive information or to impersonate the end user and continue their attack on associated businesses and entities. Phishing emails are a wide-spread business problem and can be a critical vector of attack for data breaches. This project is focused on producing a model that can be used to strengthen phishing detection using models trained on data obtained from Kaggle. This project will develop and evaluate the performance of two models: a Logistic Regression model and a Bidirectional Encoder Representation from Transformers (BERT) model. 

## Dataset
The dataset used in this project is the Phishing Email Detection found on Kaggle, uploaded by user Cyber Cop. This dataset contains two features: Email Text and Email Type. The email text feature contains the body of the email, and the email type is the associated classification label phishing or safe.

## Dependencies
<ul>
    <li>collections</li>
    <li>matplotlib</li>
    <li>nltk</li>
    <li>pandas</li>
    <li>re</li>
    <li>seaborn</li>
    <li>scikit-learn</li>
    <li>torch</li>
    <li>transformers</li>
    <li>textblob</li>
</ul>

## Findings
This project evaluated the effectiveness of detecting phishing emails using two machine learning models, Logistic Regression and BERT. Both models demonstrated high accuracy, with the Logistic Regression model achieving 97.75% accuracy and the BERT model achieving slightly better with 98.57% accuracy. The ROC AUC scores of 99% for both models demonstrate that both models have strong capability when differentiating between legitimate and phishing emails.
The models both performed very well, with the BERT model performing slightly better. However, this slight increase in performance comes at a high computational cost. The Logistic Regression model was able to compute much quicker. Considering this, the BERT model is an ideal candidate for deployment in environments where superior classification capabilities are crucial, even at a higher computational cost. The Logistic Regression model, however, is a very efficient model that still performs well and may be better for deployment in organizations that would rather balance efficiency with performance.
In conclusion, both models were capable of detecting phishing emails. While the BERT model has slightly better performance, it comes at a computational cost. Furthermore, neither model is going to identify every phishing email, so these models should not be deployed as an alternative to comprehensive user training. End users are the main target of phishing emails and through effective user training, can reduce the threat of compromise. These models, in combination with end user training offer another risk mitigation strategy for organizations to deploy to address the growing threat of phishing emails and to reduce their organization’s overall risk.
