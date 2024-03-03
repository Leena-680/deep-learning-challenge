## Overview

The purpose of this project is to create machine learning nearal network to predict applicant's chances of succeeding in their business venture. Input data is in csv file format. 

## Process
1. Begin by importing and preprocessing the dataset.
2. Preprocessing consists of removing null values and dimension reduction
3. Use preprocessed data to compile, train and evaluate the Model
4. Export the model for future use.
5. Optimise the model.

## Files and folders included in the repository  
- Resources/charity_data.csv      - This is provided input file
- deep-learning-challenge.ipynb   - This is model 1.
- deep-learning-challenge-model2  - This is model 2.
- deep-learning-challenge-model3  - This is model 3.


## Analysis
**Data Preprocessing**
Target Variable(s): The target variable for the model is the "IS_SUCCESSFUL" column, which indicates whether the funding was used effectively (1) or not (0).

Features Variable(s): The features for the model include the following columns:

APPLICATION_TYPE: Alphabet Soup application type;
AFFILIATION: Affiliated sector of industry;
CLASSIFICATION: Government organization classification;
USE_CASE: Use case for funding;
ORGANIZATION: Organization type;
INCOME_AMT: Income classification;
ASK_AMT: Funding amount requested.

Variables that should be removed from the input data because they are neither targets nor features:
"EIN" and "NAME" columns were removed for the 1st and 2nd attempts, as they were not directly linked to the probability of success. 
"SPECIAL_CONSIDERATIONS" column, additionally was removed for the 3rd attempt, it did not improve accuracy of the model.

**Model 1**  
This neural network model utilizes 2 hidden layers, because an ideal starting point for NNM’s is 2-4 layers. 
There are 43 features so 86 neurons, or 2-3 times the amount of input features were used for the first hidden node. 
The second hidden node used 43 neurons and 100 training epochs respectively. The reLU activation function was utilized, 
because it is ideal for modeling positive, nonlinear input data for classification or regression. 
The sigmoid function was utilized, because its values are normalized to a probability between 0 and 1, 
which is ideal for a binary classification dataset.

![ALT TEXT](/Assets/Model 1.png)

*Model 1 Accuracy*  

![ALT TEXT](/Assets/Acc 1.png)

**Model2**  
For this neural network model 3 hidden layers with 129, 86 and 43 neurons with 150 training epochs are used. 
The reLU activation and sigmoid functions are used.

![ALT TEXT](/Assets/Model 2.png)

*Model 2 Accuracy*

![ALT TEXT](/Assets/Acc 2.png)


**Model3**  
This neural network model utilizes 4 hidden layers with 172, 129, 86 and 43 neurons with 200 training epochs. 
The reLU activation and sigmoid functions were utilized as well.

![ALT TEXT](/Assets/Model 3.png)

*Model 3 Accuracy*

![ALT TEXT](/Assets/Acc 3.png)


**Comparison of different models**  
The first model had an accuracy score of 73.09%. After increasing the number of neurons and layers, the second model 
had an accuracy score of 72.92%. After increasing the epochs, the third model had an accuracy score of 72.47%. 
Even though third model has more hidden layers, accuracy has decreased. This indicates overfitting model.
These models did not reach the target model performance of 75%.


**Conclusion**  
*Model Overview*  
This deep learning model aimed to predict if a company would be classified as successful or no successful based 
on features of their application. Out of the three models, the highest accuracy score was 72.59% with the loss of 59.2%. 
These results are not accurate enough for the clients threshold of 75% so more modeling attempts with different 
hyperparameters would need to be built to create a more reliable binary classifier.

*Additional Model Recommendation*  
Another model that could solve this classification problem is the Perceptron or linear binary classifier. 
The perceptron model mimics a biological neuron by receiving input data, weighting the information, 
and producing a clear output. It would be a good alternative method for classification, 
because the model separates and classifies the data into two groups using linear equation. 
For the purpose of this project, those two groups would be successful and not successful.




