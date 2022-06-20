# Shopper-Retention

# *Data Science Project*
Online Shopper Intention


# Goal
Increase conversion rate using predictive model

# Objective
To get more information and analyze the factors influencing conversion rate increase
Predict whether visitors will convert or not, so that the business team can provide special treatment that is more segmented to each user.

# Stage 1: Exploratory Data Analysis <br>
<br>
<br>
<br>
<h2> Descriptive Analysis: </h2> <br>
<ol>
<li> There are no invalid entries for each feature.</li>
<li>`Administrative_Duration`, `Informational_Duration`, `ProductRelated`, `ProductRelated_Duration`, and `PageValues` features seem to have right skew distribution.</li>
<li>Some features seem to have extreme outlier values.</li>
</ol>
 
  
<h2> Categorical Analysis: </h2>
<ol>
<li>`Month` column is dominated by these value: `Mar`, `May`, `Nov`, dan `Dec` and probably it will be converted by label encoding</li>
<li>`OperatingSystems` column is dominated by these value: `Android 11`,`Android 9 and Older Ver`, and `Win 0` --> dominant value will be remain as before and the rest will be converted into `Others` Value</li>
<li>`Browser` column is dominated by `Chrome Desktop`, `Chrome Mobile`, `Firefox Desktop`, and `Samsung Internet`  --> dominant value will be remain as before and the rest will be converted into `Others` Value </li>
<li>`Region` column is dominated by oleh `Tangerang Selatan`, `Jakarta`, `Bekasi` and `Tangerang` also `Bandung`,`Semarang`, and `Surabaya` will be converted into 1 value `Luar Jabodetabek` </li>
<li>`TrafficType` is dominated by `Google.com`, `Direct Visit`, `Youtube.com`, etc --> Dominant value will be remain as before and the rest will be converted as `Others`</li>
<li>`VisitorType` column `returning_visitor` dan `new visitor` --> `others` column will be converted into most dominant value (`returning_visitor`) and also we will use label (1,0) to Encode this column </li>
<li>`Weekend` and target column `Purchase` is boolean --> it will be converted into integer boolean 1,0 </li>
 </ol>







# Stage 2: Pre Processing
<ol>
<li> Handling Duplicate </li>
125 Duplicated data has been dropped <br>
<br>
<li> Handling Outlier </li>
Using Zscore method to handling outlier <br>
<br>
<li> Drop Unused Feature </li>
PageValues and Specialday will be dropped <br>
<br>
<li> Values Feature Grouping  </li>
Cateorical values that has many unique values, the indominant values will be grouped into ‘others’ values <br>
<br>
<li> Data Type Transformation </li>
Transform boolean into integer values <br>
<br>
<li> Feature Encoding </li>
Using OHE to encode categorical vaues<br>
<br>
<li> Feature Selection </li>
Using 5 method to select the best features <br>
<br>
<li> Feature Transformation  </li>
Using logtranformation and MinMaxScaler <br>
<br>
<li> Handling Imbalance Target </li>
Using SMOTE with default sampling strategy (50:50) <br>
</ol>



# Stage 3: Modeling
<h2> We use 10 types of algorithm: </h2>
<ol>
<li>Logistic Regression </li>
<li>KNeighborsClassifier </li>
<li>GaussianNB </li>
<li>SVC </li>
<li>Decission Tree Classifier </li>
<li>Random Forest </li>
<li>Ada Boosting Classifier </li>
<li>Gradient Boosting Classifeir </li>
<li>LGBM Classifier <br>
<li>XGB Classifier </li>
</ol>


<h2> Scoring </h2>
We use F2 score to prevent many false prediction of negative label (False Negative). After hyperparameter tuning, after completing several experiment, LGBM Classifier gave the best F2 score for Train and Test score. <br>

<h2> Result </h2>
F2 Train Score : 90% <br>  
F2 Test Score: 94% <br>
<br>

<h2> Feature Importance: </h2>
ExitRates <br>
Administrative <br>
ProductRelated_Duration <br>
ProductRelated <br>
