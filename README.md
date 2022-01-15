# Neural Network Charity Analysis
![logo](images/module_19_logo.png)

# Overview

You are working with Beks, a coworker of yours, at Alphabet Soup, an organization that helps fund Charity Organizations.  You are helping Beks to evaluate the CSV given to Beks by the Alphabet Soup's business team containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.  You will be creating a machine learning algorithm, using neural networks to create a binary classifier that is capable of predicting wheter applicants will be successful if funded by Alphabet Soup.

The important metadata from this dataset captures the following about each organization:
* **EIN** and **NAME** - Identification columns
* **APPLICATION_TYPE** - Alphabet Soup application type
* **AFFILIATION** - Affiliated sector of industry
* **CLASSIFICATION** - Government organization classification
* **USE_CASE** - Use case for funding
* **ORGANIZATION** - Organization type
* **STATUS** - Active status
* **INCOME_AMT** - Income classification
* **SPECIAL_CONSIDERATIONS** - Specialconsideration for application
* **ASK_AMT** - Funding amount requested
* **IS_SUCCESSFUL** - Was the monty used effectively   

# Resources
* Data Sources: charity_data.csv
* Software: Google Colabority, Jupyter Notebook, Python 3.7, Pandas

# GitHub Application Link

<a href="https://jillibus.github.io/Neural_Network_Charity_Analysis">Neural Network Charity Analysis</a>

## Deliverable 1: Preprocessing the Data for a Neural Network Model

Data preprocessing involves transforming raw data to well-formed data sets so that data mining analytics can be applied. Raw data is often incomplete and has inconsistent formatting. The adequacy or inadequacy of data preparation has a direct correlation with the success of any project that involve data analyics.

Preprocessing involves both data validation and data imputation. The goal of data validation is to assess whether the data in question is both complete and accurate. The goal of data imputation is to correct errors and input missing values -- either manually or automatically through business process automation (BPA) programming.

Data preprocessing is used in both database-driven and rules-based applications. In machine learning (ML) processes, data preprocessing is critical for ensuring large datasets are formatted in such a way that the data they contain can be interpreted and parsed by learning algorithms. (https://www.techopedia.com/definition/14650/data-preprocessing)

Preprocessing of the Charity Data consists of:
1) Reading in the data set charity_data.csv into a pandas DataFrame.
2) Drop unnecessary columns that are not needed for the analysis, EIN and NAME.
3) Determine the number of unique values for each column.
4) Those with >10 unique values
    - Determine the number of data points for each unique value.
    - Plot the density to create a "cutoff" for rare categorical values to place in an "Others" bin
    - Validate your binning of this column worked
    - Repeat until all necessary columns are properly binned.
5) Generate a list of categorical variables.
6) Encode categorical variables using 'one-hot encoding' and place them in a new DataFrame, dropping the originals.
7) Merge the one-hot encoding DataFrame with the original DataFrame, and drop the originals.
8) Split the preprocessed data into features and target arrays.
9) Split the preprocessed data into training and testing datasets.
10) Standardize numerical variables using Scikit-Learn's _StandardScaler_ class, then scale the data.

_Lets see this in action, shall we?_

---
_1) Reading in the data set charity_data.csv into a pandas DataFrame._
<img src='images/APPLICATION_DF.png' />  

---
_2) Drop unnecessary columns that are not needed for the analysis, EIN and NAME._
<img src='images/Drop_EIN_NAME.png' />

---
_3) Determine the number of unique values for each column._
<img src='images/NUM_UNIQUE.png' />    

---
_4) Those with >10 unique values, Determine number of data points, plot density, move to bins._  
**First Column with >10 Unique Values** - APPLICATION_TYPE 
<img src='images/APPLICATION_TYPE.png' />
<img src='images/APPLICATION_TYPE_PLOT.png' />
<img src='images/APPLICATION_TYPE_BINS.png' />
  
**Second Column with >10 Unique Values** - CLASSIFICATION 
<img src='images/CLASSIFICATION.png' />
<img src='images/CLASSIFICATION_PLOT.png' />
<img src='images/CLASSIFICATION_BINS.png' />

---
_5) Generate a list of categorical variables._
<img src='images/APPLICATION_CAT.png' />

---
_6) Encode categorical variables using 'one-hot encoding' and place them in a new DataFrame, dropping the originals._
<img src='images/APPLICATION_CAT_drop.png' />

---
_7) Merge the one-hot encoding DataFrame with the original DataFrame, and drop the originals._
<img src='images/mergedDataFrame.png' />

---
_8) Split the preprocessed data into features and target arrays._  
_9) Split the preprocessed data into training and testing datasets._  
<img src='images/SPLIT.png' />

---
_10) Standardize numerical variables using Scikit-Learn's _StandardScaler_ class, then scale the data._  
<img src='images/SCALER.png' />

## For Deliverable 2: Compile, Train and Evaluate the Model

The next step in our machine learning process is to take our pre-processed datasets, now in a scaled dataframe, split into a Training and Testing setup and compile our model, train our machine with our training data, and then evaluate the model with our testing dataset.  

To do this we will follow the following steps:
1) Continue where we left off using our AlphabetSoupCharity.ipynb file.
2) Create a neural network model by assigning the number of input features and  nodes for each layer using Tensorflow Keras.
3) Create the first hidden layer and choose an appropriate activation function.
4) If necessary, add a second hidden layer with an appropriate activation function.
5) Create an output layer with an appropriate activation function.
6) Check the structure of the model.
7) Compile and train the model.
8) Create a callback that saves the model's weights every 5 epochs.
9) Evaluate the model using the test data to determine the loss and accuracy.
10) Save and export your results to an HDF5 file, naming it AlphabetSoupCharity.h5.

_Like Deliverable 1 above, lets see this in action, shall we?_

---
**FIRST RUN**  
_1) Starting in the cell after we "Scaled The Data"_  
_2) Create a neural network model by assigning the number of input features and  nodes for each layer using Tensorflow Keras._  
_3) Create the first hidden layer and choose an appropriate activation function._  
_4) If necessary, add a second hidden layer with an appropriate activation function._  
_5) Create an output layer with an appropriate activation function._  
_6) Check the structure of the model._  
<img src='images/LAYERS_1.png' />

---
_7) Compile and train the model._  
<img src='images/COMPILE_FIT_1.png' />
      
---
_9) Evaluate the model using the test data to determine the loss and accuracy._  
<img src='images/EPOCH_TEST_1.png' />

---
**SECOND RUN**  
_1) Starting in the cell after we "Scaled The Data"_  
_2) Create a neural network model by assigning the number of input features and  nodes for each layer using Tensorflow Keras._  
_3) Create the first hidden layer and choose an appropriate activation function._  
_4) If necessary, add a second hidden layer with an appropriate activation function._  
_5) Create an output layer with an appropriate activation function._  
_6) Check the structure of the model._ 
<img src='images/LAYERS_2.png' />

---
_7) Compile and train the model._   
_8) Create a callback that saves the model's weights every 5 epochs._  
<img src='images/COMPILE_CALLBACK_FIT_2.png' />

---
_9) Evaluate the model using the test data to determine the loss and accuracy._  
<img src='images/EPOCH_TEST_2.png' />

---
_10) Save and export your results to an HDF5 file, naming it AlphabetSoupCharity.h5._  
<img src='images/SAVE.png' />

---
## For Deliverable 3: Optimize your Model  
The goal for Deliverable 3 is to optimize your model and to try to get your predictive accuracy increased to over 75%.  
I will attempt to achieve this with the following:
1)  At least 3 attempts if you can't get results over 75%  
2)  Noisy variables are removed from features 
3)  Additional neurons are added to hidden layers
4)  Additional hidden layers are added 
5)  The activation function of hidden layers or output layers is changed for optimization 
6)  The model's weights are saved every 5 epochs
7)  The results are saved to an HDF5 file

_Okay, lets see this in action, shall we?_

---
_1)  At least 3 attempts if you can't get results over 75%_  
All of the PreProcess Steps above were followed, I am going to start with any **new** preprocessing steps here  

_2)  **new** Noisy variables are removed from features_  
<img src='images/ASK_AMT.png' />
<img src='images/ASK_AMT_PLOT.png' />
<img src='images/ASK_AMT_BINS.png' />

Remake of _application_cat_ dataframe to include ASK_AMT   
<img src='images/APPLICATION_CAT_OPT.png' />

Split, Train, Scale Data  
<img src='images/SPLIT_TRAIN_SCALED_OPT.png' />

---
**FIRST RUN**  
_3)  Additional neurons are added to hidden layers_  
_4)  Additional hidden layers are added_   
_5)  The activation function of hidden layers or output layers is changed for optimization_   
<img src='images/LAYERS_1_OPT.png' />

---
_6)  The model's weights are saved every 5 epochs_  
<img src='images/COMPILE_CALLBACK_FIT_1_OPT.png' />

The results for First Run  
<img src='images/EPOCH_TEST_1_OPT.png' />

---
**SECOND RUN**  
_3)  Additional neurons are added to hidden layers_  
_4)  Additional hidden layers are added_   
_5)  The activation function of hidden layers or output layers is changed for optimization_   
<img src='images/LAYERS_2_OPT.png' />

---
_6)  The model's weights are saved every 5 epochs_  
<img src='images/COMPILE_CALLBACK_FIT_2_OPT.png' />

The results for Second Run  
<img src='images/EPOCH_TEST_2_OPT.png' />  

---
**THIRD RUN**  
_3)  Additional neurons are added to hidden layers_  
_4)  Additional hidden layers are added_   
_5)  The activation function of hidden layers or output layers is changed for optimization_   
<img src='images/LAYERS_3_OPT.png' />

---
_6)  The model's weights are saved every 5 epochs_  
<img src='images/COMPILE_CALLBACK_FIT_3_OPT.png' />

The results for Third Run  
<img src='images/EPOCH_TEST_3_OPT.png' />

---
_7)  The results are saved to an HDF5 file_  
<img src='images/SAVE_Optimized.png' />

## For Deliverable 4: Results and Summary
### Results: 

* Data Preprocessing
  * What variable(s) are considered the target(s) for your model?
    * The IS_SUCCESSFUL column contains information on weither the charity has used past donations successfully. This Y/N column is considered the target column for our neural network.
  * What variable(s) are considered to be the features for your model?
    * The columns, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT will be our feature columns.  We will evaluate any of these columns and encode those needing it, then split these into training and test datasets.
  * What variable(s) are neither targets nor features, and should be removed from the input data?
    * The EIN and NAME columns are just identifier columns, so we will remove them from the dataset.
  
* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
    *  Our original attempt used 2 hidden layers with 80/30 neurons.  This provided us with input data of 43 features and 25,724 samples.
    *  The output layer was an unique neuron set as a binary classification (for the target column).
    *  I used the activation layer 'ReLU' for the hidden functions for optimization, and our output layer of 'Sigmoid' so we would have a binary classification.
    *  I used the optimizer 'adam' and the loss function 'binary_crossentropy'.     
  * Were you able to achieve the target model performance?
    *  No, I came very close and while the model was running, it would go over 75% but would end up under 75% by the end of the epoch. 
  * What steps did you take to try and increase model performance?
    *  I added additional hidden layers, increased neurons, tried the Tanh activation, as well as encoded the ASK_AMT column.   

# Summary

Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively.
The input data has 43 features and 25,724 samples.
The output layer is made of a unique neuron as it is a binary classification.
To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.
The model accuracy is under 75%. This is not a satisfying performance to help predict the outcome of the charity donations.
To increase the performance of the model, we applied bucketing to the feature ASK_AMT and organized the different values by intervals.
We increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers.
We also tried a different activation function (tanh) but none of these steps helped improve the model's performance.

The deep learning neural network model did not reach the target of 75% accuracy. Considering that this target level is pretty average we could say that the model is not outperforming.
Since we are in a binary classification situation, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.



Let me know if you have any questions or need more information.

Thank you for your time.

Jill Hughes
