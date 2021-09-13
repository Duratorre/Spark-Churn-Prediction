# Spark Churn Prediction

## Table of Contents
1. [ Installation. ](#inst)
2. [ Motivation. ](#motiv)
3. [ Data. ](#data)
4. [ Instructions. ](#ins)
5. [ Licensing, Authors, Acknowledgement. ](#lic)

<a name="inst"></a>
## 1. Installation
There are no requirements needed to run the code in this repository apart from the Anaconda distribution of Python. The code runs with no issues using the Python versions 3 and later ones. Libraries used comprise Pandas, NumPy, PySpark and Scikit-learn.

<a name="motiv"></a>
## 2. Motivation
The goal of this project is to predict customer churn, base on a set of variables related to customer characteristics and behaviour. The data is provided from Udacity and it will be used to create a ML learning pipeline to predict churn. The result of this process will be a classification model that will label new customers and determine whether they will be at churn risk.

<a name="data"></a>
## 3. Data and File Descriptions
The repository contains the following files:
  1. _mini_sparkify_event_data.json"_ contains the customer data that will be used to train and test the ML pipeline;
  2. _model.ipynb_ contains all the code used for the analysis and the development of the ML model.

<a name="ins"></a>
## 4. Instructions
To run the web app it is necessary to have python installed on your local machine. The following are the steps needed for a Linux OS. If you are using a Windows machine, the actions are the same, just remember to write the whole path to the python.exe application on your machine instead of just 'python'.

  1. Go to the project's root directory (i.e. 'cd ../project_root_directory'):
      - Run the ETL pipeline with the following command to clean and set up your database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
      - Run the ML pipeline with the following command to train the classifier and save it in a pickle file
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`      
  2. Go to the app directory ('cd ./app') and run the following command to run the web app:
        `python run.py`
  3. Go to http://localhost:3001/

<a name="data"></a>
## 5. Acknowledgements
Credit to Udacity for providing the data. Code used in this repository can be used freely.
