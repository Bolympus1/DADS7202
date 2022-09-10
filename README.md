# DADS7202 Hello World
# Traditional ML vs MLP
## 1. Dataset
diabetes _ binary _ health _ indicators _ BRFSS2015.csv is a clean dataset of 253,680 survey responses to the CDC's BRFSS2015. The target variable Diabetes_binary has 2 classes. 0 is for no diabetes, and 1 is for prediabetes or diabetes. This dataset has 21 feature variables and is not balanced.
Explore some of the following research questions:

  1.Can survey questions from the BRFSS provide accurate predictions of whether an individual has diabetes?
  2.What risk factors are most predictive of diabetes risk?
  3.Can we use a subset of the risk factors to accurately predict whether an individual has diabetes?
  4.Can we create a short form of questions from the BRFSS using feature selection to accurately predict if someone might have diabetes or is at high risk of diabetes?

Ref: https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset

# Introduction: 
This project aim to study the performance of machine learning algorithm between traditional ML and Multi Layer Perceptron (MLP) with data set "diabetes _ binary _ health _ indicators". The task is Binary classification which is evaluate model performane by F1-score.

# Assumption:
As the dataset quite big 253,680 survey and has 21 feature variables with not balanced between diabetes and non-diabetes, our assumption is MLP should show the high performance than traditional ML. 


# Exploratory data analysis :
This dataset has 21 feature variables and is not balanced. Basically we have cleansing data with explore null/duplicate/distribution and perform handle imbalanced data by using SMOTE that is the method can generate noisy samples by interpolating new points between marginal outliers and inliers. This issue can be solved by cleaning the space resulting from over-sampling.
More over, before we run traditional ML we have handle data to suitable with ML technic and maxmize F1-score. The technic that use for data preparation for traditional ML shown below table.

# Traditional ML:
We selected 4 traditional ML which is 

![image](https://user-images.githubusercontent.com/107410157/189485194-e4ac365f-7723-4966-beab-d1bffb62b412.png)

 

# MLP Network architecture:



# Training:



# Results:

# Discussion: 

# Conclusion:

# References:


# Member:


# End credit: 
This project is a part of Course DADS7202 Deep Learning, Data Analytics and Data Science, NIDA.


