# Online Shopper Purchasing Intention
A local E-Groceries named Lauk-Fresh has a problem in terms of the low conversion rate of platform visitors. As a data science team, we were asked to analyze the factors that can affect the increase in conversion rates and create a predictive model so that we can treat visitors according to the model predictions.

This project aims to increase conversion rate by 20% and increase gross profit by 15%. The data we use is data from the last 1 year which records the activities of all visitors using our platform.

The result of this project is that we managed to `increase our conversion rate` by **30.40%** and also `increase our gross profit` by **95%**. We have also analyzed the `most important factors affecting conversion rate` with their respective correlations. We also provide rational and achieveable `recommendations that can be applied by the relevant team` so that the conversion rate and gross profit of the company can increase.


# Project Background
This pandemic has had a positive impact on companies, shopping at E-Groceries is starting to become a new trend. Based on data from contentsquare, the conversion rate for E-Groceries companies increased by around 36% (2020 vs 2021). This provides great potential for Lauk-Fresh to increase its conversion rate

Currently Lauk Fresh's conversion rate is 15.63%. Our goal is to increase conversion rate by 20% and increase gross profit by 15%. This can be achieved by knowing the factors that can affect the increment of the conversion rates and implementing our recommendations in business processes.

# Dataset Overview
Our data consist of 12330 session, which are generated from our user activity on platform. There are 17 independent features and 1 target feature. Our target feature explain whether the visitor will purchase or not. 

# Pre Processing
1. Handling Duplicate
2. Feature Encoding
3. Feature Transformation
4. Handling Outlier
5. Feature Selection 
6. Handling Imbalanced Target

# Modeling
**We use 10 types of algorithm:**

1. Logistic Regression
2. KNeighborsClassifier
3. GaussianNB
4. SVC
5. Decission Tree Classifier
6. Random Forest
7. Ada Boosting Classifier
8. Gradient Boosting Classifeir
9. LGBM Classifier
10. XGB Classifier


**Scoring:**

We use F2 score to prevent many false prediction of negative label (False Negative). After hyperparameter tuning, after completing several experiment, LGBM Classifier gave the best F2 score for Train and Test score.

**Result :**
1. F2 Train Score : 90%
2. F2 Test Score: 94%

**Top 4 Feature Importance:**
1. ExitRates
2. Administrative
3. ProductRelated_Duration
4. ProductRelated

# Recommendation:
1. Discount Offering to Real-Time Non-Purchase Predicted Visitors
2. Decrease 15% Exit Rates
3. Increase 5% Administrative
4. Increase 5% Product Related Duration
5. Decrease 10% Product Related
With implement all of this recommendations, Lauk Fresh has the potential to `increase conversion rate` up to **30.40%** and `increase gross profit` by **95%**
