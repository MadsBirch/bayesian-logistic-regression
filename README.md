## Classical vs Bayesian Logistic Regression

This repository explores the differences between classical and Bayesian logistic regression for predicting the survival of passengers in the Titatnic dataset.

In this application, classical un-regularized logistic regression did not converge during maximum-likelihood estimation of the model parameters due to very rare categories in one-hot encoded columns. This is a well-known problem where very rare categories result in columns consisting off almost all 0's and model ceofficients for these variables are driven to -inf.

This problem can be solved either by imposing a small amount of model regularization or imposing priors, which are equivalent in the case of L2 regularization and Normal priors for generlized linear model.


## References:
Titatnic dataset was dowlaoaded from Kaggle: https://www.kaggle.com/datasets/yasserh/titanic-dataset
