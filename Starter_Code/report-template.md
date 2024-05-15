# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
The purpose of this analysis is to create a linear regression analysis that predicts the loan status for a borrower based on a serious of parameters. The model then predicts whether the loan status is healthy or high risk for the given borrower. Half of the data was used to train the model and thus create a linear regression model from the data. The other half was used to test the model's accuracy. 

* Explain what financial information the data was on, and what you needed to predict.
Predictions were made on a series of parameters. Those parameters were loan size, interest rate, borrower income, debt to income ratio, number of accounts, whether or not the borrower had an "derogatory marks",  and borrower's total debt. 

* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
There were 75036 loans identified as healthy and 2500 loans identified as high risk. 

* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any other algorithms).

Initially I identified the dependent variable in this case the loan status. The dependent variable or label was the status of the loan a categorical variable where 1 indicated a high risk loan, while 0 indicated a healthy loan. With the dependent variable identfied, I was able to readily identify the rest of the parameters as the independent variables or the features of this model. 

Next I split the data into to training and testing data, half of the data was used to train the model and identify an appropriate logisitcal regression to capture the results of the model. The other half was then used to test or assess the accuracy of the model. The fit() method of the LinearRegression was used to train the model. The predict () method was used to test the data. 

Then a ran a classification report to see the accuracy of the tests. 

## Results 

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
Class A (Value of 0, healthy loan status)
-Precision = 1.00 The model predicts healthy loan status with perfect accuracy. 
-Recall = .99 The recall score is nearly perfect when predicting healthy loan status. 
-f1 score = 1.00 The f1 score is perfect when assessing for "healthy" loan status in the model. 

Class B  (Value of 1, high risk loan status)
-Precision = .85 when assessing for high risk loans
-Recall = .91 when assessing for high risk loans
-F1 = .88 when assessing for high risk loans

The model is extremely reliable and extremely close to, if not perfect, when assessing for healthy loans based on the independent variables. However, it is not as reliable when determining high risk loans. Yet it is still very effective. It just cannot be relied on absolutely. 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. For example:

* Which one seems to perform best? How do you know it performs best?
It is clear that the model works best with identifying healthy loan status. 
* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
Yes, as mentioned above, performance does depend on the problem that we are trying to solve. The model gives false negatives when searching for the loan status of high risk loans, almost 15% of the data. This is an issue because identifying borrowers with high risk is a more important task than identifying borrwers with a healthy loan status. However, in saying that, the model still does predict high risk loans accurately a vast majority of the time. I think it is safe to say that this model can be used effectively but there will have to be systems in place to verify certain results associated with high risk loans. 


If you do not recommend any of the models, please justify your reasoning.
