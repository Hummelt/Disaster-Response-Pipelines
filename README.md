# Disaster-Response-Pipelines
### Web application dashboard with NLP based machine learning ETL pipeline

![Pipeline](https://files.realpython.com/media/Use-Sentiment-Analysis-With-Python-to-Classify-Reviews_Watermarked.e73ba441d870.jpg)

## Libraries
Following libraries are used in the system development:

- sys
- pandas
- re
- nltk
- sqlalchemy
- pickle
- sklearn

## Objectives
The main purpose of the ETL Disaster Response Pipeline is to separate dispatches through an algorithm and displaying the result on the screen. This is helpting to streamline the process of prioritizing messages and supplying a fast overview of the possible content (disaster category).  The application is based on NLP processing of existing messages. The machine learning process initially analyses texts which are flagged with disaster category labels and learns in this way to predict which text is linked to which disaster class.

## Approach

The ETL pipeline was initially drafted and tested in Jupyter Notebooks, then transfered to files which were in the end responsible to perform the training process.

1) The ETL pipeline consists of following process steps:

- Extract the data 
- Transform the data through data cleaning, sparating category classes, merging the information into a combined data table + saving in a sql database
- Load data into sql database 
- This process is executed in process_data.py and prepared in the Jupyter notebook ETL_Pipeline_Preparation.ipynb.

2) Machine learning process:

- Extract data from database
- Separate the disaster classes and text messages
- Split train- and test sets
- Set up NLP model
- Train model 
- Generate predictions with test data
- Evaluate model
- Adjust parameters to increase prediction accuracy
- Store model in the web application
This process is executed in train_classifier.py and prepared in the Jupyter notebook ML_Pipeline_Preparation.ipynb.

3) Flask web application:

- Form field to read in a text 
- The text is processed in the backend model
- The disaster class is highlighted 

Instructions for how to execute the app is at the end of this README.

## Data
The data is provided from Udacity and Figure Eight.

## Instructions
Instructions to use the application on a local computer:

- Run the following commands in the project's root directory to set up database and model
- Run ETL pipeline
- Run ML pipeline
- Run the following command in the command line in the app's directory
- Open new web browser and go to http://0.0.0.0:3001/
