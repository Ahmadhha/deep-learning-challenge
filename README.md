# Project Title: Deep-learning Charity Evalaution

### Shortcuts

Download Data: [csv_source](https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv)

View Base Code: [AlphabetSoupCharity.ipynb](https://github.com/Ahmadhha/deep-learning-challenge/blob/main/AlphabetSoupCharity.ipynb)

View Optimized Code: [AlphabetSoupCharity_Optimization.ipynb](https://github.com/Ahmadhha/deep-learning-challenge/blob/main/AlphabetSoupCharity_Optimization.ipynb)

View h5 files: [h5_files](https://github.com/Ahmadhha/deep-learning-challenge/tree/main/h5_files)

View Optimized h5 files: [Optimized_h5_files](https://github.com/Ahmadhha/deep-learning-challenge/tree/main/h5_files_optimization)

## Backgroud:

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures.

## Description: 

Training and evaluating a neural-network based binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Scope: 

Creating a neural-network machine learning model and optimizing it to improve the perofrmance to a recommended target of 75%. 

## Dataset:

CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. 

#### Features:

- EIN and NAME—Identification columns

- APPLICATION_TYPE—Alphabet Soup application type

- AFFILIATION—Affiliated sector of industry

- CLASSIFICATION—Government organization classification

- USE_CASE—Use case for funding

- ORGANIZATION—Organization type

- STATUS—Active status

- INCOME_AMT—Income classification

- SPECIAL_CONSIDERATIONS—Special considerations for application

- ASK_AMT—Funding amount requested

- IS_SUCCESSFUL—Was the money used effectively

# Report:

### Overview

Purpose of Analysis: To predict the success of a charity organization based on historic features of previous projects.

### Results

* Data Preprocessing: 

  - Target Variables: 'IS_SUCCESSFUL' feature, which is a binary value that indicates whether the money was used effectively or not
  
  - Features: All remaining columns other than the target column and the 'EIN' and 'NAME' columnms. The columns are increased to 44 after one-hot encoding
  
  - Removed Columns: EIN and NAME, they are neither targets nor features.

* Compiling, Training, and Evaluating the Model

  - First Model Description:
  
    * Layers: 2
   
    * Nodes: 16, 8
    
    * epochs: 20
   
    * Activation Function: 'relu'
   
  - First Model Description:
  
    * Layers: 4
   
    * Nodes: 32, 16, 8, 4
    
    * epochs: 50
   
    * Activation Function: 'swish'

  - Results Accuracy: 

    * First model: Accuracy: 72.5% Loss: 0.56
   
    * Second model: Accuracy: 72.9% Loss: 0.56
    
    * Target accuracy was not achieved
 
  - Optimization steps: The second model uses more nodes in the original 2 layers, adds 2 more layers, increases the epochs in addition to changing the activation function in an attempt to increase the accuracy.

### Summary

While the accuracy appears to improve for the second model it is not by a significant amount, the additional resources and processing time it requires are not justified.

A different model that can be used in the Random Forest Algorithm.

Random Forest is an machine learning model that combines multiple decision trees to make predictions. It works by training each tree on a random subset of the data and features, and then aggregating the predictions of all the trees to make a final prediction. 

It could be a better alternative to Neural-Networks because it is more interpretable, robust to noise and outliers, and more scalable as it is relatively quicker to train.

However, it is prudent to mention that the better is at the end problem and dataset specific, and the only way to find out with certainty is  to try multiple models and compare their performance.
