# README

## Dataset information:
The diabetes data set was collected from 130 US hospitals over almost 10 years (1999-2008). This data set includes 50 different features. The detailed information for each feature can be found [here](https://www.hindawi.com/journals/bmri/2014/781670/tab1/). The data sets can be downloaded [here](https://archive.ics.uci.edu/ml/datasets/diabetes+130-us+hospitals+for+years+1999-2008).

## Problem statements:
This project deals with the readmission rate of diabetes patients. When the diabetes patients are admitted to a hospital, they get treated and discharged. What you don’t want is they will require readmission because that is a waste of money and resources and it’s also not good care. I think in this problem we will care more about false negative, which means that people was predicted to not require readmission while the reality is otherwise. 

- Goal:  Use this data set and apply machine learning algorithms to predict whether a future patient will be readmitted or not. This will help save the cost and improve the care condition.

## Files: 
- Readme: you are reading this file
- diabetes\_data.csv: Data file.
- admission\_mapping.csv: Second part of data for types of admission
- Diabetes\_visualize\_model.ipynb: Python jupyter notebook for visualization and modeling data
                                         
## Required libraries to run this project: 
    1. Numpy
    2. Pandas
    3. Matplotlib
    4. SKlearn
    5. Seaborn

## Summary/Discussion:
In this project, I used Logistics Regression, Adaboosted classifier and Random Forest classifier to predict whether a diabetes patient will experience readmission. I used GridSearchCV to tuen hyperparameters on Adaboosted to improve the performance of model.
    * The performances of all models are very similarly with accuraries ranging from 61% to 64%. The tuned Adaboost and Random Forest have the best performance (~64%). This accuracy level is not very good YET. It requires more work to improve.
    * Looking at the confusion-matrix, precision, recall and F1-score for each model, I can see that the false negative is very big, which means recall for ‘readmission’ is low. However, they differ quite a lot between models (The readmission Recall of Logistic Regressioin is 39% while that of Random Forest is 52%). Even though this recall is very low and needs to be improved, I think that Random Forest gives us the best performance in terms of both accuracy and readmission recall.  
    * To improve the performance of model on this data I need to spend more time to find the pattern and optimize the feature selection. I am also thinking about reducing the number of dimensions of features. Improving the parameter tuning process and applying cross validation may also help.
