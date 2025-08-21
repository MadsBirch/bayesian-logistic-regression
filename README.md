## Classical vs Bayesian Logistic Regression

This repository explores the differences between classical and Bayesian logistic regression for predicting the survival of passengers in the Titanic dataset.

### Convergence
In this application, classical unregularized logistic regression did not converge during maximum-likelihood estimation of the model parameters due to very rare categories in one-hot encoded columns. This well-known problem occurs when rare categories produce columns consisting mostly of zeros, causing the corresponding model coefficients to diverge toward −∞.

This problem can be solved by imposing a small amount of regularization or by specifying priors, which are equivalent in the case of L2 regularization and Normal priors in generalized linear models.

### Prior, likelihood and posterior distributions
I illustrate the role of the prior and likelihood distributions and their effect on the posterior distribution, under different prior strengths and varying dataset sizes.

### Parameter and prediction uncertainty
Finally, I show how uncertainty in the model parameters propagates into the predictive distribution. The predictive distribution for a new data point $(x^*, y^*)$ is obtained by integrating over the posterior distribution of the model parameters, thereby incorporating parameter uncertainty:

$$
\begin{aligned}
p(y^*=1 \mid \ y, x^*) = \int p(y^*=1 \mid \ x^*) p(\beta \mid y) d \beta,
\end{aligned}
$$


### References:
Titatnic dataset was dowlaoaded from Kaggle: https://www.kaggle.com/datasets/yasserh/titanic-dataset
