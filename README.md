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
* Reading in the data set charity_data.csv into a pandas DataFrame
* Drop unnecessary columns that are not needed for the analysis, EIN and NAME.
* Determine the number of unique values for each column
 * Those with >10 unique values, 
 * Determine the number of data points for each unique value.
 * Plot the density to create a "cutoff" for rare categorical values to place in an "Others" bin
 * Validate your binning of this column worked
 * Repeat until all necessary columns are properly binned.
* Generate a list of categorical variables
 * Encode categorical variables using 'one-hot encoding' and place them in a new DataFrame, dropping the originals

_Lets see this in action, shall we?_

---
<img src='images/application_df.png width=50% height=50%'/>    <img src='images/Drop_EIN_NAME.png width=50% height=50%'/>

---

<img src='images/NUM_UNIQUE.png width=50% height=50%'/>    <img src='images/Drop_EIN_NAME.png width=50% height=50%'/>

---

<img src="images/cryptonames_df.head.png"/>

---
```

```
<img src="images/X.head.png"/>

---


## For Deliverable 2: Compile, Train and Evaluate the Model


<img src="images/pcs_df.nopredictions.png"/>


```
<img src="images/elbow_curve.png"/>

---
## For Deliverable 3: Optimize your Model
At least 3 attempts if you can't get results over 75%
Noisy variables are removed from features (2.5 pt)
Additional neurons are added to hidden layers (2.5 pt)
Additional hidden layers are added (5 pt)
The activation function of hidden layers or output layers is changed for optimization (5 pt)
The model's weights are saved every 5 epochs (2.5 pt)
The results are saved to an HDF5 file (2.5 pt)
<img src="images/predictions.png"/>

---
```

```
<img src="images/pcs_df.head.png"/>

---
```

```
<img src="images/clustered_df.head.png"/>

## For Deliverable 4: Results and Summary
### Results: 

* Data Preprocessing
  * What variable(s) are considered the target(s) for your model?
  * What variable(s) are considered to be the features for your model?
  * What variable(s) are neither targets nor features, and should be removed from the input data?
  
* Compiling, Training, and Evaluating the Model
  * How many neurons, layers, and activation functions did you select for your neural network model, and why?
  * Were you able to achieve the target model performance?
  * What steps did you take to try and increase model performance?

```

```
<img src="images/clustered_df.plot.png"/>

---
```

```
<img src="images/clustered_df.table.png"/>

---
```

```
```

```
---
```

```
```

```
<img src="images/plot_df.head.png"/>

---
<img src="images/plot_df.png"/>

# Summary

Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.



Let me know if you have any questions or need more information.

Thank you for your time.

Jill Hughes
