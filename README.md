# Sales prediction for food items sold at various retail store outlets
## Food Item sales and the features that impact the sales.

**Author**: Pieter Slabber

![alt text](https://github.com/SlabberP/Prediction-of-Product-Sales/blob/main/data-scientist.jpg)

### Business problem:

The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.


### Data:
Data Source: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

### Data Dictionary:
The data consists of columns containing information regarding different products and stores.
![alt text](https://github.com/SlabberP/Prediction-of-Product-Sales/blob/main/Data%20Dictionary.GIF)

The dataframe was found to have 8523 rows and 12 columns

## Methods:
- Data preparation steps:
  - The data was cleaned using the normal removal of the duplicate values.
  - It was then checked for inconsistencies. The inconsistencies were fixed.
  - The "Item_Outlet_Sales" column or feature was then identified as the target or dependent column.
  - Check the data for null values or missing values. Imputing these values only happens after the train/test split.
  - Split the train and test data.
  - Preprocessing:
     - Creating pipelines for encoding and scaling of Categorical, Ordinal and Numerical features.
     - Fit the preprocessor to the traing data only
     - Transform the training and test data
  
- Machine Learning:
  - The model was based on the independant and dependent features which is a regression target.
  - Instantiate the Model:
  - Fit the model to the training data only
  - Train the Model on the training data
  - Test the Model
  - Tune the Model and test again
  - Evaluate the model performance using metrics
    
## Visuals:     
### Countplot
![alt text](https://github.com/SlabberP/Prediction-of-Product-Sales/blob/main/CountPlot.png)

One can see that the 3 highest count of Item_types kept in the stores are:
- Fruits and Vegetables,
- Snack Food and
- Household items

### Heatmap
![alt text](https://github.com/SlabberP/Prediction-of-Product-Sales/blob/main/Heatmap.png)

From the heatmap one can see that there is a high correlation between Item_Outlet_Sales and Item_MRP features.

## Models evaluated and results: 

- Linear Regression Model
  Training R-squared: 0.6715387235708582
  Test R-squared: -4.948580222595302e+18
  The model might be overfitting because it makes good predictions on the training data but not on the test data.
  
- Random Forest Model

  Training Data:
  - MAE = 297.065
  - MSE = 184,186.360
  - RMSE = 429.169
  - R^2 = 0.938
  
  Test Data:
  - MAE = 773.962
  - MSE = 1,241,180.546
  - RMSE = 1,114.083
  - R^2 = 0.550
  The model might be overfitting as well because it makes good predictions on the training data but not on the test data.

- Random Forest Model Hypertuned with GridSearchCV

  Training Data:
  - MAE = 665.766
  - MSE = 899,797.137
  - RMSE = 948.576
  - R^2 = 0.696 
  
  Test Data:
  - MAE = 732.864
  - MSE = 1,114,327.909
  - RMSE = 1,055.617
  - R^2 = 0.596
    
The final Random Forest regression model shows favorable performance metrics on both training and test data. 
Its ability to minimize errors, provide accurate price predictions, and explain a substantial portion of price variability makes it a valuable tool for solving the business problem of predicting product prices. 

## Recommendations:

The recommendation will be to use the Random Forest Model because it gave the best results, however 
by further tuning the Randon Forest Model one should be able to get even better results.

Overfitting can be reduced by decreasing the complexity of the model. 

Adding more data to the training set should also reduce overfitting.

### For further information

For any additional questions, please contact **pieter.slabber@mmltd.co.za**
