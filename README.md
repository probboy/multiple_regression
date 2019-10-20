# multiple_regression
Multiple Regression Analysis for the Kings County Housing Price


We conducted multiple regressioin analysis on the King's county housing price. 

First of all, we want to eliminate multicolinearity in the dataset, by looking at the heat map below.

![alt text](https://github.com/probboy/multiple_regression/blob/master/heatmap.png "Logo Title Text 1")

In preparation for multiple linear regression, we need to fix the heteroscedasticity problem in the data set. Compare the the two set of residual plots below, one before the Box-Cox power transformation (on the price variable), the next one after the Box-Cox power transformation.

![alt text](https://github.com/probboy/multiple_regression/blob/master/Homoscedasticity0.png "Logo Title Text 1")

![alt text](https://github.com/probboy/multiple_regression/blob/master/Homoscedasticity1.png "Logo Title Text 1")

As we see above, better homoscedasticity is achieved after the Box-Cox power transformation.

Similarly, the Box-Cox transformation restore normality in the data, as you can see by comparing the two graphs below.

![alt text](https://github.com/probboy/multiple_regression/blob/master/QQ0.png "Logo Title Text 1")

![alt text](https://github.com/probboy/multiple_regression/blob/master/QQ1.png "Logo Title Text 1")

We also convert the 'zipcode' variable into a dummy variable in our regression analysis before carrying out OLS regression results:

![alt text](https://github.com/probboy/multiple_regression/blob/master/OLS0.png "Logo Title Text 1")

Finally we want to do a 80/20 split to show that there is no problem of overfitting. The OLS regression on the training dataset is as follows:

![alt text](https://github.com/probboy/multiple_regression/blob/master/OLS_train.png "Logo Title Text 1")

The MSE of the testing data set is 14.071, and the MSE of the training data set is 14.072, thus there is no overfitting, and regularization is not needed.
