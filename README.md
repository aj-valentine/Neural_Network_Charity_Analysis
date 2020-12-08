# Non-profit Analysis using Neural Network Models :brain:
## Analyzing whether non-profit applicants will be successful with neural network models

## Overview of the Non-Profit Analysis

The purpose of this analysis is to create various neural network learning models to predict whether a certain company will be successful if chosen to for funding by the Alphabet Soup company. The analysis involves a binary classifier that will predict whether the companies will be successful or not. The neural network model analyzes 34,000 past records of organizations that have received funding from Alphabet Soup if they failed or succeeded. The CSV file also contains many other metrics about the companies: name, application type, affiliation, classification, use case for funding, organization type, status, income classification, special considerations for application, funding amount requested, along with whether they were successful or not in using their money effectively. 

The first part of the analysis involves the preprocessing step for the data. In this step, the data is cleaned, bucketed into specific categories,  and  categorically encoded to allow the model to read the different categories. Once the data is ready to use, the second step involves prepping the binary classification model using TensorFlow. The model is first created by determining the number of inputs, the number of neurons and the number of hidden layers. Once this is established, the model is evaluated by determining its loss and accuracy levels of predicting the success rate of funded companies. 

The tools used in this analysis are: Python and TensorFlow with Neural Network Models in Jupyter Notebook. 

## Results 

1. Data Preprocessing:

What variables are considered the targets for your model? 
- In the neural network model, the target of the analysis is variable y: whether or not the application is successful. In other words, the target is to figure out whether the model can accurately predict whether or not the company will be successful and use the funding money effectively. 

What variables are considered to be the features for your model? 
- The X variable is the feature for the model. X is made up of the features of the dataset that do not include y. In this case, the features of the model are: application type, affiliation, classification, use case for funding, organization type, status, income classification, special considerations for application, and funding amount requested. 

What variables are neither targets nor features and should be removed from the input data? 
- The two variables that are dropped in the beginning of the data preprocessing step are: EIN and Name. These are dropped because they do not provide the model with any additional data to help it predict successful funding. 

2. Compiling, Training, and Evaluating the Model: 


How many neurons, layers, and activation functions did you select for your neural network model and why? 
- In the fsecond optimization version of the model, the amount of inputs were the length of the training set of X. The first layer had 125 neurons, the second 60, and the third also 60. Overall, there were 15,906 total parameters. 

-- insert screen shot

Were you able to achieve the target model performance? 
- With many different types of adjustments, the best performance reached with the model was 73% accuracy and loss 56%. Before the adjustments, the model was performing at 45% accuracy and 76% loss. 

-- insert screen shot

-- insert screen shot

What steps did you take to try and increase model performance? 
- The following steps were taken in order to reach the 73% accuracy level: 
    1. Dropped more inputs (columns) in the dataset: special considerations and use case 
    2. Added additional neurons to all hidden layers 
    3. Added an additional hidden layer
    4. Changed the Tensorflow epocs number from 100 to 150


## Summary 

In conclusion, the Neural Network model achieved the best accuracy level at 73% - which is not even close to many standards for a successful model. Overall, this model would not be used in a professional setting since the accuracy level is not => 95%. However, the increase from original 45% to 73% accuracy level was significant with the changes that were implemented. A better model for this dataset would be Random Forest Classification model. Because the dataset only includes   34,000 data points, it would be better suited with Random Forest. Neural Network models are very powerful, and should be used for data with at least 100,000 points. 
