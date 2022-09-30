# Neural Network Charity Analysis

## Overview
* This project will utilize machine learning and neural networks in order to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup, a non-profit foundation. The goal of this classifier it to achieve results over 75%. 

## Results
### Data Preprocessing
* The variable that is the target in the model is "IS_SUCCESSFUL".
![target]()
* The variables that are the features for the model are: "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT".
![features]()
* Variables that are neither targets nor features, and were removed from the input data are: "EIN", and "NAME".
![drop_columns]()
### Compiling, Training, Evaluating the Model
* The initial model was comprised of two hidden layers which were comprised of 80 and 50 neurons. This is a larger dataset and selecting values gives us a total of 7,621 trainable parameteres. The activation used was ReLu due to the fact that no feature data was valued below 0. The output layer's activation was selected as sigmoid as we were looking for a binary output. 
![initial]()
* The model was only able to achieve a 72.43% accuracy rate which is 3% below our goal of 75% accuracy.
* In order to attempt to increase the model's performance, three variations of the model were created and tested. The various methods included increasing the number of neurons, adding additional hidden layers, and utilizing an optimizer. The optimizer was given three activators to utilize as well as ranges for nodes and hidden layers. Through its randomized trials of various methods, it was unable to achieve a 75% accuracy rate. 
* The first trial increased the neurons to 100 per layer whiched increased our parameters to 14,601.
![trial1]()
* The second trial added an third hidden ReLu layer with 50 additional neurons increasing the trainable parameters to 19,601.
![trial2]()
* The third attempt to increase performance was to utilize a Keras optimizer. This optimizer utilized ReLu, Tanh, and Sigmoid activations and was allowed up to 6 hidden layers. The optimizer tried variations of activators, layers, and neurons in order to see which combination would work best. 
![trial3]()
## Summary
* Many methods were utilized for testing our deep learning model. Variations in nodes, epochs, and the addition of hidden layers were utilized as well. Even through these methods, an accuacy rate of 75% was not achievable. It would be recommended to try further cleaning of data in order to remove additional features that may be throwing off our models. This would potentially allow for an accuracy rate of at least 75%. 
