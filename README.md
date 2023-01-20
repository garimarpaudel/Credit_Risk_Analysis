# Credit_Risk_Analysis
Supervised Machine Learning Challenge

## Overview
### 
Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. The goal of this project is to build a classification model that can predict if an applicant is likely to have low or high credit risk. The credit card company can use this information to determine whether or not an applicant should be approved. We will employ different techniques to train and evaluate models with unbalanced classes and evaluate models using resampling. We will then evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, we’ll oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, we use a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, we compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Lastly, we evaluate the performance of these models and make a written recommendation on whether they should be used to predict credit risk.

## Results

### Naive Random Oversampling
The first model was trained with data sampled using the naive random overampling technique. In random oversampling, instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced. Oversampling addresses class imbalance by duplicating or mimicking existing data.

* Balanced Accuracy Score: 0.6519805729802466

* Confusion Matrix: 

![image](https://user-images.githubusercontent.com/108683284/213616096-804bd7e2-1956-498a-80cf-b656a9260a1c.png)

* Classification Report:

![image](https://user-images.githubusercontent.com/108683284/213615643-d6e7555b-7b13-4cab-8457-954bb877fbc9.png)

### SMOTE Oversampling
The synthetic minority oversampling technique (SMOTE) is another oversampling approach to deal with unbalanced datasets. In SMOTE, like random oversampling, the size of the minority is increased. 

* Balanced Accuracy Score: 0.6463291312633204

* Confusion Matrix:

![image](https://user-images.githubusercontent.com/108683284/213616623-83a13951-b85e-47ee-be42-a6a4d9facbbc.png)

* Classification Report:

![image](https://user-images.githubusercontent.com/108683284/213616504-e984f89c-8510-4ab3-b118-12c1da5caa74.png)

### Undersampling
Undersampling is another technique to address class imbalance. Undersampling takes the opposite approach of oversampling. Instead of increasing the number of the minority class, the size of the majority class is decreased. Undersampling only uses actual data.

* Balanced Accuracy Score: 0.6519805729802466

* Confusion Matrix:

![image](https://user-images.githubusercontent.com/108683284/213616834-498c0dbc-f068-4c33-8b7d-bf85ad8d7733.png)

* Classification Report:

![image](https://user-images.githubusercontent.com/108683284/213616939-b9e76916-2cd7-4b1f-b6e1-1bcc8159cadf.png)

### Combination Sampling
* Balanced Accuracy Score: 0.6276665820612302

* Confusion Matrix:

![image](https://user-images.githubusercontent.com/108683284/213617225-69578282-1bac-4571-9daf-9b428024f17c.png)

* Classification Report:

![image](https://user-images.githubusercontent.com/108683284/213617272-ddcbdcfb-0d93-4477-b477-93f81068bf08.png)

### Balanced Random Forest Classifier
This method improves overall model performance by combining multiple models to help improve accuracty and decrease variance. The Random Forests Classifier is composed of several small decision trees created from random sampling. By using the Balanced Random Forests, we oversample from the minority class to balance the classes.

* Balanced Accuracy Score: 0.7885466545953005

* Confusion Matrix:

![image](https://user-images.githubusercontent.com/108683284/213617639-cc69499d-8022-4e9d-b445-51d1deac6015.png)

* Classification Report:

![image](https://user-images.githubusercontent.com/108683284/213617603-df0e418d-a21f-4ded-a619-cc39fe0fda02.png)

### Easy Ensemble AdaBoost Classifier
Using AdaBoost, a model is trained and then evaluated. The errors of the first model are given extra weight when the subsequent model is trained and so on until the error rate is minimized.

* Balanced Accuracy Score: 0.9316600714093861

* Confusion Matrix:

![image](https://user-images.githubusercontent.com/108683284/213617998-dbbb3f32-71ee-491c-bd59-06ac402d2b52.png)


* Classification Report:

![image](https://user-images.githubusercontent.com/108683284/213617912-3b455700-4b10-4f3a-902d-1d23eec12c0c.png)


## Summary
In this dataset, we find that the best model to use is the "Easy Ensemble AdaBoost Classifier" because not only does it have a high accuracy score, but it also has the best precision and sensitivity (recall) especially in terms of correctly identifying high-risk applicants. Therefore, we would reccomend using this model to predict credit risk.
