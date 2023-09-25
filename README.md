# Machine Learning - Project 2 Car Insurance Claim Prediction

**Author**: Pieter Slabber

![alt text](https://github.com/SlabberP/Machine-Learning-Practice-Solutions/blob/main/carInsur.jpg)

### Dataset: Car Insurance Claim Prediction

#### Source of the data:

https://www.kaggle.com/datasets/sagnik1511/car-insurance-data 

#### Brief Description of the data:
Context:

The company has shared its annual car insurance data. Now, you have to find out the real customer behaviors over the data.

Content
The columns are resembling practical world features.
The outcome column indicates 1 if a customer has claimed his/her loan else 0.
The data has 19 features from there 18 of them are corresponding logs which were taken by the company.

#### Target:
The target is the 'Outcome' column which is a binary classification answer.

#### Data:
This is business data

#### Problem:
This is a classification problem. The outcome column indicates 1 if a customer has claimed his/her loan else 0.

#### Features:
The data consists of 19 features.

#### Rows :
The dataset consists of 10000 rows.

#### Challenges with cleaning the data:
I need to decide to remove some of the features and also Which inconsistencies exists. This could be a challenging dataset but it is close to a real world example as one can get.

### Methods:
Data preparation steps:

#### Delete unnecessary columns:
Both ID and POSTAL_CODE columns were dropped because it should not make a difference in predicting the target - Outcome column.

#### Check for duplicates
20 duplicate rows were found and removed.

#### Identified and addressed missing values
It was found that two columns contain null values. The two columns are CREDIT_SCORE and ANNUAL_MILEAGE.
It was decided the best value for both column missing values was the mean value. This is the only value that make sense for both columns.

#### Identified and corrected inconsistencies in data for categorical values
No inconsistencies found in the Categorical columns.

### Visuals:

### Heatmap

![alt text](https://github.com/SlabberP/Machine-Learning-Practice-Solutions/blob/main/HeatMap.PNG)

Summary of correlations between Features and the target:

The lighter the heatmap colour is, the higher the correlation is. In other words, the closer to 1.0 the higher the correlation.

I can see there is a high correlation between PAST_ACCIDENTS and SPEEDING_VIOLATIONS which makes perfect sense.

I can also see a correlation between MARRIED and VEHICLE_OWNERSHIP which also makes sense.

A humorous correlation is between SPEEDING_VIOLATION and CHILDREN.

I can also see a correlation between VEHICLE_OWNERSHIP and CREDIT_SCORE which also makes sense.

Unfortunately it is difficult to find any correlation between the feautures and the target(OUTCOME) looking at the heatmap.

### Regression Plot

![alt text](https://github.com/SlabberP/Machine-Learning-Practice-Solutions/blob/main/Regression_Plot.PNG)

If you look at the above graph one can clearly see that the more people that drive under the influence(DUIS), the more accidents are caused by them which is very clear in relationship between the two columns and the black regression line. In reality it makes sense when people drive under the influence of alcohol or drugs that the chances to make an accident is bigger that if the drive sober. This will obviously cause more claims by die driver and these people are a risk for the Car Insurance company.

### Bar Plot

![alt text](https://github.com/SlabberP/Machine-Learning-Practice-Solutions/blob/main/Bar_Plot.PNG)

One can also clearly see that the PAST_ACCIDENTS goes up with more SPEEDING_VIOLATIONS. The more a driver is speeding and get a fine the higher chances are that the accidents will occur and therefor the claims will also increase. These people are risks for the Car insurance company.

### Metrics for the best model
Train Report
              precision    recall  f1-score   support

           0       0.87      0.90      0.88      5146
           1       0.76      0.71      0.73      2339

    accuracy                           0.84      7485
   macro avg       0.81      0.80      0.81      7485
weighted avg       0.84      0.84      0.84      7485

Test Report
              precision    recall  f1-score   support

           0       0.89      0.90      0.90      1716
           1       0.78      0.76      0.77       779

    accuracy                           0.86      2495
   macro avg       0.83      0.83      0.83      2495
weighted avg       0.86      0.86      0.86      2495

KNN and Logistic Regression models we tested against the data and the KNN model with out hypertuning perfomed the best.



For any additional questions, please contact **pieter.slabber@mmltd.co.za**
