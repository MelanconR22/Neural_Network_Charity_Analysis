# Neural_Network_Charity_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

AlphabetSoup is a philantrhopic foundation dedicated to helping organizations that help the environment, improve people's well-being, and unify the world.  AlphabetSoup has raised and donated over 10 billion dollars over the last 20 years.  I have been asked to study the impact that donations provide and to predict which organizations are worth donating to and which organizations are too high risk.  To perform this task, I will design and train a deep learning neural network to evaluate data to produce a clear decision making result.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

## Results: Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
##### What variable(s) are considered the target(s) for your model?
* The target variable for this model is the IS_SUCCESSFUL column.
*
##### What variable(s) are considered to be the features for your model?
* APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT are variables that are considered to be features for the model.

##### What variable(s) are neither targets nor features, and should be removed from the input data?
* For this project, EIN and NAME are neither targets nor features and were removed from the input data.

### Compiling, Training, and Evaluating the Model
##### How many neurons, layers, and activation functions did you select for your neural network model, and why?
##### Were you able to achieve the target model performance?
##### What steps did you take to try and increase model performance?
## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
