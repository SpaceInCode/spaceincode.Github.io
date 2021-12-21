---
title: overfitting and underfitting
date: 2021-06-15
categories: Machine Learning
---


Here's the takeaway: Models can suffer from either:

- **Overfitting:** capturing spurious patterns that won't recur in the future, leading to less accurate predictions, or
- **Underfitting:** failing to capture relevant patterns, again leading to less accurate predictions.

**Overfitting** is a model matches the training data almost perfectly, but does poorly in validation and other new data.

When a model fails to capture important distinctions and patterns in the data, so it performs poorly even in training data, that is called **underfitting**. Result predictions may be far off for most houses, even in the training data.

The criterion to distinguish the fitting property is **MAE**.
