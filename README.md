# Neural_Network_Charity_Analysis

## Overview
The purpose of this analysis is to predict if an Alphabet Soup-funded organization will be successful based upon features in the dataset. This is explored via the creation and training of a binary classification model.

## Results
### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
  - The target variable is considered to be IS_SUCCESSFUL.
- What variable(s) are considered to be the features for your model?
  - The features of the model are STATUS, ASK_AMT, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and SPECIAL CONSIDERATIONS. In other words, each of the following lines other than IS_SUCCESSFUL.
  - ![Features](https://github.com/kramerkyle/Neural_Network_Charity_Analysis/blob/main/Dataframe_Features.png)
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - EIN, NAME, and APPLICATION_TYPE are neither. APPLICATION_TYPE was removed in the optimization process but failed to improve the model.

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - 3 layers: Initial, Hidden, Output
  - 80 initial neurons, 30 for the hidden layer
  - The activation functions were: relu, relu, and sigmoid, respectively.
  - ![Model](https://github.com/kramerkyle/Neural_Network_Charity_Analysis/blob/main/Model.png)
- Were you able to achieve the target model performance?
  - Target performance was not able to be achieved
- What steps did you take to try and increase model performance?
  - An additional variable, APPLICATION_TYPE, was dropped due to its number of unique values
  - 4 layers: Initial, Hidden, Hidden, Output
  - 80 initial neurons, 40 for each other layer
  - The activation functions were changed to: relu, tanh, tanh, tanh, and sigmoid, respectively.

## Summary
This process failed to cross the 75% accuracy goal. The initial deep learning model was able to classify results correctly 73% of the time with a loss of 0.56. After optimization attempts the accuracy was slightly lower at ~71% with a loss of 0.56.

A logistic regression model could be employed to better solve the classification problem. This would increase the interpretability of the results and simplify the process.
