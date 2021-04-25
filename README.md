# Data Scientist Nanodegree Capstone Project
This project is a machine learning model that can correlate the mobile features and prices with the mobile popularity in the market then predict the popularity for other mobile phones. The details of the project implementation and results are available in the file Capstone_Project_Discussion.pdf

## Contents

The repo consists of the below files:

* 01_Data_ETL_Preparation_NB.ipynb - The Data processing Notebook
* 02_Dataset_Data_Analytics_NB.ipynb - Data Analytics Notebook
* 03_ML_Model_NB.ipynb - Machine Learning Model Notebook
* Capstone_DS.zip - Datasets Zip Folder (To be extracted)
* Capstone_Project_Discussion.pdf - A blog for all the steps in the project and the results
* README.md

## Code Flow and Results

The code cleans data extracted from 3 dataset which are:
- Amazon Cell Phones Reviews
- Amazon Reviews: Unlocked Mobile Phones 
- GSMArena

Two datasets are the reference for mobile popularity and price while the third one is the reference for the mobile features

After that, K-Nearest Neighbors Regressor is used to predict the mobile popularity using the mobile price, battery life and body weight. Logarithmic transformation and MinMaxScaler are used to enhance the data training. GridSearch is used to find the best parameters for the regressor and the results was using 38 n_neighbours and distance weights. To enhance the model further, BaggingRegressor with 100 estimators is used to enhance the performance of the KNN Regressor.

![alt text](https://github.com/fatma-hassanein/Data_Scientist_Nanodegree_Capstone_Project/blob/main/results.png)

The root of mean squared error reached 0.542 for the test dataframe and 0.19 for the training dataframe.

### Instructions:
1. Extract the datasets zip folder "Capstone_DS.zip"
2. Run the three notebooks in order to perform the three steps of the model and produce the final results:

- 01_Data_ETL_Preparation_NB.ipynb
- 02_Dataset_Data_Analytics_NB.ipynb
- 03_ML_Model_NB.ipynb

### Dependencies

* Python
* pandas
* numpy
* seaborn
* sklearn
* scipy
* sqlalchemy
