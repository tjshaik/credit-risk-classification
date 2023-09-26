# Report

## Overview of the Analysis
The purpose of the analysis to predict the status of the loan, if its going to be a healthy loan or a high risk loan based on various factors. These variables include interest rate, borrower income, debt to income, number of accounts among other things. The following are steps you need to take to predict if a loan is healthy or high risk. First you a clean dataset with variables that are going to used to predict the risk and a column that states the actual result(loan_status). In a new dataframe you remove the column with the actualy result(loan_status) and then split the data in to training and test set, .75/.25. Then you fit the logistic regression model on the training set, then use that to predict on the testing set. Logistic regression model in a supervised learning ML that is used to predict the probablity of a certain class based on dependent variable. Then you evaluate the model performance using a confusion matrix which shows the number of true pos, false pos, true neg and false neg. You can also evaluate the model by checking its accuracy, F1, recall (accuracy of postive predictions)and precsion(postive prediction out of all predictions). 


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Logistic Regression results 
- Accuracy scores: .99
- Precision: 1 for classifying the healthy loans and .85 for classifying the high risk loans 
- Recall: .99 for classifying the healthy loans and .91 for classifying the high risk loans  


## Summary
This model has an accuracy of .99 and correctly predicts high risk loans with a recall of .91 and precision of .85. This a reliant model which high metrics. Having false postive for high risk in this case is safe than than having a false negative from a bank's perspective. It is more important that we have a high recall and precision for predicting 1's (high risk) to be are on the safer side.  Also there is most likly a high precision and recall for predicting healthy loans because there are more healthy loans than high risk loans in the dataset. To improve this model we could stratify for loan status. You can also change the threshold for the classifcation, or change your training/test set to be .8/.2 and see if it improves the model.
