# Assignment-19
AlphabetSoup Neural Network and ML

## Overview 

The purpose of this analysis is to create a binary classifier to predict,
if an applicant (a business entity) will be successful or not if funded by Alphabet Soup. The dataset contains over 34,000 organizations that have been funded by alphabet soup. There are a number of columns that capture the metadata of each organization such as organization type, the use of funding amongst others. This project is comprised of 3 steps: Preprocessing the data for the neural network, Compile,train and evaluate the model & finally optimizing the model.

## Results:
#### Data Preprocessing

- variable(s) that are considered the target(s) for your model?
The variable we are targeting in this module is the IS_SUCCESSFUL column.
- variable(s) that are considered to be the features for your model
The features that we are using are every column except the ones that we will drop.
- What variable(s) are neither targets nor features were removed
First features we drop are the 'EIN' & 'NAME' because we expect both features to have little to do with our outcome.Compiling, Training, and Evaluating the Model

#### Compiling, Training, and Evaluating the Model
- Number of neurons, layers, and activation functions selected? 
The initial model includes a single input features & two hidden layers. The first hidden layer has 50 neurons, the second has 25. Additionally, each of the hidden layers employed the "relu" activation method, while the output layer employed the "sigmoid" activation.
- Were you able to achieve the target model performance? 
The 75% target was not reached. The first model only achieved a 46.6% accuracy rate.
![image](https://user-images.githubusercontent.com/80020446/128876920-4ba37100-edc8-4b71-ba88-fd85a1f0f923.png)

- What steps did you take to try and increase model performance?
1. Optimization 1: Reduced the application_counts to less than 500 and the classification_counts to les than 800; increased neurons to 80 and 30 respectively.

2. Optimization 2: Dropped SPECIAL_CONSIDERATIONS feature because of prevalance of "N" for the value, returned application_counts to less than 700 and classification_counts to less than 1800.

3. Optimization 3: Dropped the third hidden layer and changed the activation method for the output layer to "tanh"
![image](https://user-images.githubusercontent.com/80020446/128876394-7528df1d-890f-4649-a1cc-670bf0df4483.png)

## Summary

The models accuracy ended up being 72.8% - we started with a data set and tried to predict whether or not the project would be successful on all of the features that we used after dropping two features that we figured to be irrelevant. Although I did not get to the accuracy of 75% that I wanted it is possible the reason for this is we may have had to drop more features which may have affected how good the neural network actually is. The best way to increase the accuracy of your model is to have more data. If we have solid data added to this model, the accuracy of this model will be much more concrete.
