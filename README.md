# Spark Churn Prediction

## Table of Contents
1. [ Installation. ](#inst)
2. [ Motivation. ](#motiv)
3. [ Data. ](#data)
4. [ Summary. ](#sum)
5. [ Licensing, Authors, Acknowledgement. ](#lic)

<a name="inst"></a>
## 1. Installation
There are no requirements needed to run the code in this repository apart from the Anaconda distribution of Python. The code runs with no issues using the Python versions 3 and later ones. Libraries used comprise Pandas, NumPy, PySpark and Scikit-learn.

<a name="motiv"></a>
## 2. Motivation
The goal of this project is to predict customer churn, base on a set of variables related to customer characteristics and behaviour. The data is provided from Udacity and it will be used to create a ML learning pipeline to predict churn. The result of this process will be a classification model that will label new customers and determine whether they will be at churn risk.

<a name="data"></a>
## 3. Data and File Descriptions
The repository contains the following file:
  - _model.ipynb_ contains all the code used for the analysis and the development of the ML model.

<a name="sum"></a>
## 4. Result
The entire dataset of Sparkify is 12GB, however in this project we will analyze only a small subset (128MB) of the full dataset, in order to derive a predictive model to run and test against the full dataset.

For Sparkify, around 20% of the users decide to churn. Users who churn are more predominantly males. Users who churn show less involvement with Sparkify.

Two approaches are taken, one that consider total variables like total songs played, total songs liked, total seconds of song played, etc., whereas the second focus on variables that are more dependant on the sessions of each user, like average songs played per session, average number of songs liked per session, or average time gap between sessions.

Among the two approaches taken, the one that takes into account all the information regarding user sessions, like session average duration and average gap between sessions shows the best results.
The features that are the best predictors of churn risk, i.e. have the best correlation with churn, are the total time a user has been subscribed to the service and the average time gap between sessions.

Different algorithms are tested, such as Random Forest(RF), Linear Regression (LR), Linear SVC (LSVC). The dataset is heavily imbalanced towards not churn users (almost 80% of the cases), therefore we introduce class weights to deal with class imbalance. Moreover, we make use of Cross-Validation to tune the parameters of the used estimators.
The best algorithm is Linear Regression with weight column to handle class imbalance and with values of accuracy, recall, precision and f1 score of 0.85.

<a name="data"></a>
## 5. Acknowledgements
Credit to Udacity for providing the data. Code used in this repository can be used freely.
