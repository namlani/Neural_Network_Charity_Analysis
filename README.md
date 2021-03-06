# Neural_Network_Charity_Analysis
## Overview
The purpose of this analysis is to use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Results
### Data Preprocessing
* What variable(s) are considered the target(s) for your model?
  <br>The "IS_SUCCESSFUL" column
* What variable(s) are considered to be the features for your model?
  <br>All columns except for the "EIN" and "NAME" columns
* What variable(s) are neither targets nor features, and should be removed from the input data?
  <br>"EIN" and "Name"
  
### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
  <br>1st Hidden Layer: 8 neurons and relu activation function
  <br>2nd Hidden Layer: 5 neurons and relu activation function
  <br>Output layer: sigmoid activation function
  
  This model was chosen because relu is considered to be more efficient with nonlinear data and the second layer can re-weigh the inputs from the first layer. Performance metrics from this model: 
  <br>![image](https://user-images.githubusercontent.com/5934390/125510754-bb760bf3-cb55-47ef-913a-d2430e0e9b9d.png)

* Were you able to achieve the target model performance?
  <br>No
* What steps did you take to try and increase model performance?
  1. Added a neuron and changed activation function to sigmoid for the second layer:
     <br>!![image](https://user-images.githubusercontent.com/5934390/125522480-002a6caf-9577-4fc4-82a8-af59c95b85f6.png)
  2. Added a third layer using sigmoid with 6 neurons
     <br>![image](https://user-images.githubusercontent.com/5934390/125522158-ffcebf5b-1541-47cf-b086-8291fd1f3eed.png)
  3. Dropped SPECIAL_CONSIDERATIONS and STATUS columns:
     <br>![image](https://user-images.githubusercontent.com/5934390/125523320-e880cdc1-6c61-461a-aaeb-3336497ef6ef.png)

## Summary
The model was unable to reach an accuracy rating of 75% after using working code that makes three attempts to increase performance using the following steps:
  * Noisy variables are removed from features
  * Additional neurons are added to hidden layers
  * Additional hidden layers are added
  * The activation function of hidden layers or output layers is changed for optimization
  * The model's weights are saved every 5 epochs
  * The results are saved to an HDF5 file

Because removing variables, using different activation functions and different amounts of layers and neurons did not achieve the intended results, conducting additional research on activation functions and the effects different combinations of the number of neurons and layers have is recommended. 
