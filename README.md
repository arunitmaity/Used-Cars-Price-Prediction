# Used-Cars-Price-Prediction
This repository contains all files related to the project titled 'Used Cars Price Prediction' for COMS 4995 - Applied Machine Learning 

### Objective
The used car market is large nowadays, and the used quotes given by car sellers and buyers are manually provided or given with their hidden algorithm. It is not easy for the average person to get an accurate and transparent used car estimation without going to the dealership. This project tries to find an algorithm that can estimate used car prices without human involvement. Additionally, we can discover the essential attributes that can affect used car price listing with interpretable machine learning models.

### Data Set
The dataset is readily available on Kaggle and is the collection of prices of the used cars listed on Craiglist.org. It is a collection of .csv files that has size of nearly 1.45 GB.
https://www.kaggle.com/austinreese/craigslist-carstrucks-data

### Methodology
We tried out eight different techniques and optimized the model using GridSearchCV and Regularization wherever applicable. The Linear Regression model has the lowest complexity; however, it had a sub-par performance in our scenario compared to models with higher complexity. This might be because we apply various pre-processing strategies such as Ordinal and One-Hot encoding and aggregation of variable values. This shows that the target variable does not have a direct linear relationship with all the columns, and thus we require a more complex model to map the inputs to the target variable. Even the optimized decision tree regressor could only attain a sub-par R2 score since a single tree algorithm overfits the data. As expected, higher complexity tree-based models such as Random Forest Regressor, Histogram Gradient Boosted Regressor, XGBoost Regressor, and CatBoost Regressor tend to perform much better than linear models. In our case, the best performance was achieved using the XGBoost Regressor with a training R2 score of 0.9406 and a testing R2 score of 0.8074. To make the model deployable in a real-world scenario, we decided to choose an XGBoost Regressor with a lesser number of estimators (500) compared to our highest performing regressor with 2000 estimators since the R2 score difference was marginal (0.03). This was done to reduce the overall model complexity, thereby deeming it appropriate for deployment.
   


** NOTE **
In order to read about the project and our proposed methodology refer to the PDF file titled 'Use Cars Price Prediction Project Report.pdf'.
