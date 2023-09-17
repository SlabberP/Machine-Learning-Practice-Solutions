# Machine Learning - Project 2

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

#### Methods:
Data preparation steps:

The data was cleaned using the normal removal of the duplicate values.
It was then checked for inconsistencies. The inconsistencies were fixed.
The "Item_Outlet_Sales" column or feature was then identified as the target or dependent column.
Check the data for null values or missing values. Imputing these values only happens after the train/test split.
Split the train and test data.
Preprocessing:
Creating pipelines for encoding and scaling of Categorical, Ordinal and Numerical features.
Fit the preprocessor to the traing data only
Transform the training and test data
Machine Learning:

The model was based on the independant and dependent features which is a regression target.
Instantiate the Model:
Fit the model to the training data only
Train the Model on the training data
Test the Model
Tune the Model and test again
Evaluate the model performance using metrics

For any additional questions, please contact **pieter.slabber@mmltd.co.za**
