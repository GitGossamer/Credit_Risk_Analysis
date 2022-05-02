# Credit_Risk_Analysis
# Overview of the loan prediction risk analysis
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. With this in mind, this analysis was designed to assess credit risk for the variety of loan options available. We’ll apply different techniques to train and evaluate models with unbalanced classes. Jill has specifically asked us to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.
Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we’ll use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we will compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. This document is a written recommendation on whether they should be used to predict credit risk.

## Results: There is a bulleted list that describes the balanced accuracy score and the precision and recall scores of all six machine learning models (15 pt)

Naïve Random Oversampling
 ![Naive Random Oversampling](https://user-images.githubusercontent.com/96449605/166182684-b4866c98-15b9-4a94-8d8f-b9ab3e6f7d4f.png)

•	Balanced Accuracy Score: ~ 0.625
•	Precision Score: The precision of 0.99 is low for High-risk loans and is high for Low-risk loans.
•	Recall Score: High/Low risk = 0.60/0.65, with an overall recall score of 0.65
•	F1 Score: 0.78
SMOTE Oversampling
 ![SMOTE Oversampling](https://user-images.githubusercontent.com/96449605/166182697-c15f632b-e04d-4810-bb2f-1be5b9ef87a6.png)

•	Balanced Accuracy Score: ~ 0.651
•	Precision Score: The precision of 0.99 is low for High-risk loans and is high for Low-risk loans.
•	Recall Score: High/Low risk = 0.64/0.66, with an overall recall score of 0.66
•	F1 Score: 0.79
Undersampling
 ![Undersampling](https://user-images.githubusercontent.com/96449605/166182728-a2d91d28-cf3c-4b00-8067-482f50f54c07.png)

•	Balanced Accuracy Score: ~ 0.651
•	Precision Score: The precision of 0.99 is low for High-risk loans and is high for Low-risk loans.
•	Recall Score: High/Low risk = 0.61/0.45, with an overall recall score of 0.45
•	F1 Score: 0.62

Combination Under-Over Sampling
 ![Combination Under_Over](https://user-images.githubusercontent.com/96449605/166182752-48626512-2004-42a4-b109-98e4b54f5d1f.png)

•	Balanced Accuracy Score: ~ 0.529
•	Precision Score: The precision of 0.99 is low for High-risk loans and is high for Low-risk loans.
•	Recall Score: High/Low risk = 0.72/0.58, with an overall recall score of 0.58
•	F1 Score: 0.73

Balanced Random Forest Classifier
 ![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/96449605/166182787-750c767f-1f8d-4803-bc85-7dfe2902bf5c.png)

•	Balanced Accuracy Score: ~ 0.672
•	Precision Score: The precision of 1.0 is low for High-risk loans and is high for Low-risk loans.
•	Recall Score: High/Low risk = .34/1.0, with an overall recall score of 1.0
•	F1 Score: 1.0, this appears to be the best of our tested models due to the F1 score being more balanced (but still favoring low risk loan applications).

Easy Ensample AdaBoost Classifier
 ![Easy Ensample AdaBoost](https://user-images.githubusercontent.com/96449605/166182818-bdc76409-bf68-488d-8791-4e5a9725c50b.png)

•	Balanced Accuracy Score: ~ 0.919
•	Precision Score: The precision of 0.99 is low for High-risk loans and is high for Low-risk loans.
•	Recall Score: High/Low risk = .90/.94, with an overall recall score of 0.94.
•	F1 Score: 0.97

### Summary: 
After reviewing the array of machine learning models used to analyze credit risk data, it would appear the Balanced Random Forest Classifier provides the best results. While all precision scores tended to lean towards an average of .99, this was mainly due to the larger low risk score which brings the average up significantly. It’s worth noting that there is some disparity in the size of the data set, which leads to the idea that more research is warranted for a better model.
