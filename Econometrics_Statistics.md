Estimation techniques vs times series models
There are time series models (such as VAR, ARIMA, etc.) and there are estimation techniques
(such as OLS, maximum likelihood (ML), etc.). Different models can be estimated by different techniques
(sometimes more than one). E.g. a VAR can be estimated by OLS or ML while ARIMA (with a nonempty MA part)
cannot be estimated by OLS but can be estimated by ML.

When modelling some data, you need to choose a sensible model and then estimate it. The choice of a sensible model may
be hard, I would say, much harder than the estimation of the chosen model. But once the choice is done, you proceed to 
estimation. If you choose a VAR, then you can estimate it by OLS.

Indeed, as Matthew Gunn says,Estimating VAR models with ordinary least squares is a commonplace, perfectly 
acceptable practice in finance and economics.And as Christoph Hanck correctly adds,if typical VAR assumptions
are met (i.e., each equation has the same regressors, the errors are mean independent of the lagged variables
- i.e., you got the dynamics right), OLS is even the efficient systems estimator.

Thus the statement OLS is not sophisticated enough for time series analysis is simply not true in general.

The Confusion Matrix (Evaluating performance for classification problems)
￼
Is important to note that there is a tradeoff between precision/recall. So when training our model we need to check if
typeI or typeII error is more important. 

Recall is the true positives divided by true positives + false negatives 
Precision is the true positives divided by true positives +false positives
Accuracy is correct predictions divided by all predictions

F1-score is the harmonic mean of precision and recall and punishes big mistakes in the predictions
F1-score= 2*((precision*recall)/(precision+recall)) 

Evaluating performance for regression problems
Mean Absolute Error 
Mean Squared Error (The one I used) MSE
Root Mean Squared Error (I used too)

The machine learning process
￼
In Python, we use Scikit-Learn Library to train data to create a model

CHOOSING AN ALGORITHM (classification or clustering or regression or etc)

￼


The MLE is concerned about choosing the parameter which can maximize the likelihood or equivalently the
log-likelihood function. And then fit the model based on the trial estimated parameter value and calculate
the mean of the model. To find the iterative weighted and working dependence and based on this two and the
design matrix we can estimate the best parameter value.

The OLS will take the parameter value which minimize the error ( residuals) of the model. It will take into 
acount that the residual sum of square and derivate with respect to the parameter regression coefficient 
(beta) and set it to zero and then we will find the parameter value which minimize the error(residual sum of square).


Training methods: MAE, MSE, RMSE
Estimation Methods for training parameters: OLS, MLE, GLS
Methods to estimate the models: adjusted R-squared, AIC, BIC, RMSE, MAE