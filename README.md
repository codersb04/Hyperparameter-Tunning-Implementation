# Hyperparameter-Tunning-Implementation
## Task
Build a Machine Learning model for Breast Cancer Prediction using Hyperparameter Tunning for Support Vector Classifier.</br>
Tool Used: Jupyter Notebook, Python
## Hyperparameter Tunning
Hyperparameter Tunning is a process of choosing optimum set of parameters for Machine Learning Model. This process is also know as "Hyperparameter Optimizatiom". There are two type of Hyperparameter Tunning:
1. GridSearchCV: In this Each of the parameter is taken each. The processing time and cost are more in this.
2. RandomizedSearchCV: In this some random parameter values are taken to get the calculate optimized parameters values for the model
## Working
- Import all the necessary libraries
- Load the dataset to pandas DataFrame from CSV file using read_csv function of pandas
- Analyse the data and check for missing values
- Convert the Categorical Text data to numeric: B: 0 and M: 1
- Split the features(all the features except id, diagnosis and Unnammed: 32) and Target(Diagnosis)
- Convert them to numpy array
- K-Fold Cross Validation is used to increase the accuracy
- Load the Support Vector Classifier
- Define the parameters for the classifier
- Fit the model using Grid search CV: GridSearchCV(model, parameters, cv=5)
- The results are:
  - Highest Accuracy = 95.26%
  - Best Parameters = {'C':5,'kernel':'linear'}
- Load the SVC again
- Fit the model using Randomized Search CV: RandomizedSearchCV(model, parameters, cv=5)
- The results are:
  - Highest Accuracy: 95.08%
  - Best Parameters: {'kernel': 'linear', 'C': 20}
- Built the model using train test spit method and use the optimized parameter to load the model.
  - Accuracy score of SVC model with Best parameters:  93.86 </br></br></br>

Reference: 8.4. GridSearchCV and RandomizedSearchCV - Python implementation | Hyperparameter Tuning, Siddhardhan, https://www.youtube.com/watch?v=aijB8qbEOQ4&list=PLfFghEzKVmjsNtIRwErklMAN8nJmebB0I&index=121
