---
layout: post
title: Regression Project
---
This project reads in a data set on cost of living in 2018. Cost of living and rent index is used as an explanatory variable to predict cost of living index. In order to find the right model, the redundant column is dropped and the names of the columns are adjusted to make the columns more accessible. The data is being logged to reduce the skew. Then the data is plotted and different degrees of polynomial models are evaluated. It turned out that 1st degree polynomial fits the data well. Pipeline is applied to scale the data and RidgeCV is used to find the appropriate alpha, intercept and coefficient. Lastly, the model is found and the R^2 and MSE values are calculated. 