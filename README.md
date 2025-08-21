## Classical vs Bayesian Logistic Regression

This repository explores the differences between classical and Bayesian logistic regression for predicting the survival of passengers in the Titatnic dataset.

### Convergence
In this application, classical un-regularized logistic regression did not converge during maximum-likelihood estimation of the model parameters due to very rare categories in one-hot encoded columns. This is a well-known problem where very rare categories result in columns consisting off almost all 0's and model ceofficients for these variables are driven to -inf.

This problem can be solved either by imposing a small amount of model regularization or imposing priors, which are equivalent in the case of L2 regularization and Normal priors for generlized linear model.

### Prior, likelihood and posterior distributions
I show the role of the prior and likelihood distribbution and their effect on the posterior distribution for different strengths of the prior and for different amount of datapoint.

### Parameter and prediction uncertainty
Finally, I show how the uncertainty w.r.t. to the model parameters is carried all the way through to the predictive distribution. The predictive distribution for new data point $(x^*, y^*)$ is given by the weighted sum over the posterior distribution of the model parameters and thereby contains the uncertainty w.r.t. model parameters

$$
\begin{align}
p(y^*=1 \mid \ y, x^*) &= \int p(y^*=1 \mid \ x^*) p(\beta \mid y) d \beta,
\end{align}
$$


### References:
Titatnic dataset was dowlaoaded from Kaggle: https://www.kaggle.com/datasets/yasserh/titanic-dataset
