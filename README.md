# TimeSeriesAnalysis
This dataset 'train_target1.xlsx' contains data from x1 to x29 (features) and 'target1' for specific datetime. The purpose of this code is to predict 'target1' and compare different prediction methods to determine the optimal forecasting method.

# Exploring data
The first step is to present 'target1' on the distribution plot.\
Data is standardized using StandardScaler() to convert it on a unit scale (mean=0 and variance=1) as it is a condition for optimal performance of many machine learning algorithms.\
Principal Component Analysis (PCA) is used to reduce the number of variables from 29 to 2 to visualize the data.\
Outlier observations are removed using sigma_clip() and drop() functions to eliminate the heavy tails of the 'target1' distribution plot.\
Finally, the data is split into:
- train1 (includes all observations from September)
- train2 (includes all observations from August)
- test1 (includes all observations from August).

# Model comparison
The comparison of prediction methods is based on:
- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- Median Absolute Error (MedAE).

We compare the following models:
- Random Forest
- K-Nearest Neighbors
- Linear Regression
- Ridge Regression
- Lasso Regression
- Elastic Net Regression
- Support Vector Machine.

The model with the lowest MSE, MAE, and MedAE values is selected as the optimal forecasting method.\
Based on the error metrics, the random forest regression outperforms other models. The table that shows the actual and predicted values for each model and each instance is also helpful to understand the performance of the models. Overall, the code is well-organized and easy to follow.
