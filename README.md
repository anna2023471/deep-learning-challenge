# deep-learning-challenge

# Overview

The purpose of this analysis was to create a neural network model that could predict the success of applicants funded by Alphabet Soup. The analysis was performed using a datastet of over 34,000 records. Tensorflow Keras was used to create a sequential model. The target prediction accuracy of the model was 75% and above.

# Results

## Data Preprocessing

* The target for the model was the success or failure of each applicant (represented as the binary column "IS_SUCCESSFUL" with 0=No and 1=Yes).
  
* The features for the model were:
  
  * APPLICATION_TYPE — Alphabet Soup application type
  
  * AFFILIATION — Affiliated sector of industry
  
  * CLASSIFICATION — Government organisation classification

  * USE_CASE — Use case for funding
  
  * ORGANIZATION — Organisation type
  
  * STATUS — Active status
  
  * INCOME_AMT — Income classification
  
  * SPECIAL_CONSIDERATIONS — Special considerations for application
  
  * ASK_AMT — Funding amount requested

* The following variables were removed as they were neither features nor targets:
 
  * EIN - Identification column
   
  * NAME - Identificayion column
   
  ## Compiling, Training, and Evaluating the Model

* The final model consisted of 50 input dimensions, three hidden layers, and one output layer. The hidden layers had 200, 100, and 50 neurons respectively; the output layer had one neuron. The following activation functions were used:
    
  * First hidden layer - relu
        
  * Second hidden layer - tanh
        
  * Third hidden layer - relu
        
  * Output layer - sigmoid
   
* The model was not able to achieve target performance of over 75% accuracy, with the best performing model achieving only 73.2%.
    
* Various steps were taken to optimise model performance, including:
 
  * Removing features deemed unnecessary and increasing the number of rare variable bins
   
  * Increasing the number of hidden layers
   
  * Increasing the number of neurons in each layer
   
  * Increasing the number of epochs
   
  * Using a different activation function in one of the hidden layers
   
# Summary

Despite multiple attempts at optimising the model, performance could not be increased above 73%. Regardless of the steps taken to optimise the model, no significant improvement in performance was observed in any of the steps. A Support Vector Model (SVM) may be better suited to this task. Unlike a neural network, SVMs are not limited to the input feature dimensions and can use an ulimited number of dimensions to find a solution.
