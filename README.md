# Neural_Network_Charity_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

AlphabetSoup is a philantrhopic foundation dedicated to helping organizations that help the environment, improve people's well-being, and unify the world.  AlphabetSoup has raised and donated over 10 billion dollars over the last 20 years.  I have been asked to study the impact that donations provide and to predict which organizations are worth donating to and which organizations are too high risk.  To perform this task, I will use the features in the provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

This analysis will use a csv from Alphabet Soup's business team that contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively

## Results: Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
##### What variable(s) are considered the target(s) for your model?
* The target variable for this model is the IS_SUCCESSFUL column.

##### What variable(s) are considered to be the features for your model?
* APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT are variables that are considered to be features for the model.

##### What variable(s) are neither targets nor features, and should be removed from the input data?
* For this project, EIN and NAME are neither targets nor features and were removed from the input data.

### Compiling, Training, and Evaluating the Model
##### How many neurons, layers, and activation functions did you select for your neural network model, and why? Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

* The original model has input features and two hidden layers.  The first hidden layer has 3 neurons while the second hidden layer has 1 neuron.  The number of neurons was selected in an effort to be as efficient and use as few resources as possible. The original model used relu activation functions for the hidden layers and sigmoid activation function for the output.  This was chosen to allow the data to be learned as classification or regression but the output was desired to be a binary classification.

![model1](https://user-images.githubusercontent.com/107599510/200913253-d48ed241-3eaa-43ce-ad9b-2e57e5cb1c1a.png)

* The original attempt resulted in an accuracy score of 0.7209 which did not meet the 0.75 target performance.

![score1](https://user-images.githubusercontent.com/107599510/200917108-f945d4bd-2f25-4116-85d8-ac88cb350ddf.png)

* This model did achieve the first 0.75 accuracy score on epoch 20 and achieved an accuracy of 0.8438 on epoch 24.  That was the highest accuracy score for an epoch during the 100 epochs that were tested.

#### 1st Optimization Attempt - How many neurons, layers, and activation functions did you select for your neural network model, and why? Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

* The first optimization attempt used the same hidden layers and neurons but changed all of the activation functions to sigmoid due to the desired output being a binary classification.

![model2](https://user-images.githubusercontent.com/107599510/200916458-3797a0b2-50ee-43c1-a51d-3088f0757315.png)

* This attempt resulted in a slightly higher accuracy score of 0.7247 but ended up short of the desired 0.75 target score.

![score2](https://user-images.githubusercontent.com/107599510/200917503-799e02a7-f433-4145-9008-b063e6490f52.png)

* This model did achieve the first 0.7571 accuracy score on epoch 17 and achieved an accuracy of 0.9062 on epoch 69.  That was the highest accuracy score for an epoch during the 100 epochs that were tested.

#### 2nd Optimization Attempt - How many neurons, layers, and activation functions did you select for your neural network model, and why? Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

* The second optimization attempt used 10 neurons in the first hidden layer and 3 neurons in the second hidden later.  The two hidden layers were activated with the sigmoid funciton and the output layer was activated with the relu function.  This was chosen to be the opposite of the original model to see if the accuracy score would increase.  

![model3](https://user-images.githubusercontent.com/107599510/200919683-ef674457-6349-4eda-a0ba-84f301f44c57.png)

* The accuracy of this model dropped to 0.7202 which is short of the desired 0.75 target score.

![score3](https://user-images.githubusercontent.com/107599510/200919941-c6ae253c-2901-445d-b6d1-fd279d2c02cc.png)

* This model did achieve the first 0.75 accuracy score on epoch 15 and achieved an accuracy of 0.8125 on epoch 47.  That was the highest accuracy score for an epoch during the 100 epochs that were tested.

#### 3rd Optimization Attempt - How many neurons, layers, and activation functions did you select for your neural network model, and why? Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

* The third optimization attempt used 25 neurons in the first hidden layer and 7 neurons in the second hidden later.  The two hidden layers were activated with the sigmoid funciton and the output layer was activated with the relu function.  This was chosen to be the opposite of the original model to see if the accuracy score would increase.  Additionally, the epochs were increased from 100 to 300 to see if additional learning would help. 

![model4](https://user-images.githubusercontent.com/107599510/200922552-bf9ab194-4d43-4ae8-8352-191025e5266d.png)

* The accuracy of this model came in at the highest mark of 0.7254 but was still short of the desired 0.75 target score.

![score4](https://user-images.githubusercontent.com/107599510/200922980-d1d10c2f-68de-40f1-b0c2-3f8b49216343.png)

* This model did achieve the first score above 0.75 which was 0.7677 accuracy score on epoch 16.  Additionally, the model achieved an accuracy of 0.8125 on epoch 19 with the highest accuracy score of 0.8438 on epoch 248.   That was the highest accuracy score for an epoch during the 300 epochs that were tested.

## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

The model did not achieve the desired target score.  This set of data might be better classified using the tanh activation function with sigmoid output.  There could also be room to remove the SPECIAL_CONSIDERATIONS feature to see if the data becomes easier to classify.  The models also seemed to reach desired accuracy in a short amount of epochs so running the model with less epochs could produce higher accuracy numbers.

