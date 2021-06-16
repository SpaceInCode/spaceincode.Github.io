---
title: python in machine learning 
layout: post
categories: Machine Learning
date: 2021-06-15
---


There are some codes for [[machine learning]] course on the Kaggle.

## basic data exploration

```python
# pandas is used in operate dataframe
import pandas as pd
# numpy is used to calculate numbers with special functions
import numpy as np
```

The most important part of the Pandas library is the [[DataFrame]]. A DataFrame holds the type of data you might think of as a table.

```python
# read the data and store data in DataFrame titled melbourne_data
melbourne_data = pd.read_csv(melbourne_file_path)
# print a summary of the data in Melbourne data
melbourne_data.describe()
```

## To choose variables/columns

We'll need to see a list of all columns in the dataset. That is done with the **columns/features** property of the DataFrame.

```python
melbourne_data.columns
# dropna drops missing values (think of na as "not available")
melbourne_data = melbourne_data.dropna(axis=0)
```

## Selecting The Prediction Target.

You can pull out a variable with **dot-notation**. This single column is stored in a **Series**, which is broadly like a DataFrame with only a single column of data.

```python
y = melbourne_data.Price
# choose features
melbourne_features=['Rooms','Bathroom']
X = melbourne_data[melbourne_features]
```

## Delete missing value columns

```python
# Get names of columns with missing values
cols_with_missing = [col for col in X_train.columns
                     if X_train[col].isnull().any()]

# Drop columns in training and validation data
reduced_X_train = X_train.drop(cols_with_missing, axis=1)
reduced_X_valid = X_valid.drop(cols_with_missing, axis=1)
```

This uses `drop` function to delete columns.

## machine learning model

Example of [[Building Model]] with [[scikit-learn]],

```python
from sklearn.tree import DecisionTreeRegressor
# Define model. Specify a number for random_state to ensure same results each run
melbourne_model = DecisionTreeRegressor(random_state=1)
# Fit model
melbourne_model.fit(X, y)
```

Specifying a number for `random_state` ensures you get the same results in each run.

We now have a fitted model that we can use to make predictions.

```python
print("Making predictions for the following 5 houses:")
print(X.head())
print("The predictions are")
print(melbourne_model.predict(X.head()))
```

## [[model validation]]

There are many metrics for summarizing model quality, but we'll start with one called **Mean Absolute Error** (also called **MAE**), and error=actual−predicted.
Once we have a model, here is how we calculate the mean absolute error:

```python
from sklearn.metrics import mean_absolute_error
predicted_home_prices = melbourne_model.predict(X)
mean_absolute_error(y, predicted_home_prices)
```

- [[validation data]]
- [[training data]]

```python
# split the data
train_X, val_X, train_y, val_y = train_test_split(X, y, random_state = 0)
# Define model
melbourne_model = DecisionTreeRegressor()
# Fit model
melbourne_model.fit(train_X, train_y)
# get predicted prices on validation data
val_predictions = melbourne_model.predict(val_X)
print(mean_absolute_error(val_y, val_predictions))
```

## other topics

[[overfitting and underfitting]]
[[random forest]]
If you keep modeling, you can learn more models with even better performance, but many of those are sensitive to getting the right parameters.
