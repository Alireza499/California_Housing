# California Housing Price Prediction



## Overview

This project focuses on predicting housing prices in California using machine learning techniques. We'll explore various regression models, data preprocessing, and performance evaluation methods to achieve accurate predictions.

## Included Libraries

- `numpy` for numerical operations
- `pandas` for data manipulation
- `matplotlib` for data visualization
- `seaborn` for enhancing data visualization

## Dataset

We use the `california_housing` dataset from `sklearn.datasets` and convert it into pandas dataframes according to dataset guidelines.

## Renaming Feature Columns

We rename feature columns to enhance readability and understanding.

## Data Exploration

Initial data exploration reveals that `MedInc` and `Age` have a significant influence on house values. We observe a linear relationship between `Rooms` and `Bedrooms`, suggesting that one of them could be removed without significant data loss.

## Preprocessing

- Checked for missing values (NAN), which were not found.
- Normalized the data using the `StandardScaler`, except for the target column.

## Outliers

We identified outliers using box plots and decided to remove them from our dataset.

## Data Splitting

We divided the dataset into target and feature columns.

## Model Selection

This is a supervised regression problem, and we explored various regression models:

1. Linear Regression
   - Achieved a score of 0.6315072660252627.

2. Polynomial Regression
   - RMSE (Root Mean Square Error) on the test set: 5.670315284384829 (indicating overfitting).

3. RandomForestRegressor
   - Achieved a score of 0.7974259906553882.

4. BayesianRidge
   - Achieved a score of 0.631466335376941.

## K Fold Cross Validation

We applied K Fold Cross Validation to assess model performance.

## Ensembles

a- Bagging
   - Utilized the `BaggingClassifier` with a score of 0.6322518816498772.

b- Boosting
   - XGBoost (eXtreme Gradient Boosting) achieved a score of 0.8313086213535643.

## Conclusion

The project demonstrates the effectiveness of machine learning techniques in predicting California housing prices:

- XGBoost (eXtreme Gradient Boosting) achieved the highest accuracy score of 83% with an RMSE of 0.47.
- Simpler models like linear regression and BayesianRidge achieved scores around 63.
- Bagging and boosting algorithms, such as Random Forest, are recommended for this problem.

For Random Forest, further data preprocessing and parameter tuning could lead to even better results.

In summary:

- XGBoost: RMSE - 0.47495883799834593
- BayesianRidge: RMSE - 0.7020177813591233
- Random Forest: RMSE - 0.5204768187936862, Score - 0.7974259906553882
- Linear Regression: RMSE - 0.7019787959914987, Score - 0.6315072660252627

## License

This project is licensed under the MIT license. For more information, please refer to the license file.

---

Feel free to explore the Colab notebook, contribute to the project, or adapt the techniques for your own regression problems!
