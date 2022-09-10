# DADS7202
# Traditional ML vs MLP
## 1. Dataset
diabetes _ binary _ health _ indicators _ BRFSS2015.csv is a clean dataset of 253,680 survey responses to the CDC's BRFSS2015. The target variable Diabetes_binary has 2 classes. 0 is for no diabetes, and 1 is for prediabetes or diabetes. This dataset has 21 feature variables and is not balanced.
Explore some of the following research questions:

  1. Can survey questions from the BRFSS provide accurate predictions of whether an individual has diabetes?
  2. What risk factors are most predictive of diabetes risk?
  3. Can we use a subset of the risk factors to accurately predict whether an individual has diabetes?
  4. Can we create a short form of questions from the BRFSS using feature selection to accurately predict if someone might have diabetes or is at high risk of diabetes?

Ref: https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset

# Introduction: 
This project aims to study the performance of machine learning algorithms between traditional ML and Multi-Layer Perceptron (MLP) with data set "diabetes _ binary _ health _ indicators". The task is Binary classification which evaluates model performane by F1-score.

# Assumption:
As the dataset is quite big 253,680 surveys and has 21 feature variables with not balanced between diabetes and non-diabetes, we assume that MLP should show a high performance than traditional ML. 


# Exploratory data analysis :
This dataset has 21 feature variables and is not balanced. We have cleansed data by exploring null/duplicate/distribution and perform handle imbalanced data by using SMOTE which is the method that can generate noisy samples by interpolating new points between marginal outliers and inliers. This issue can be solved by cleaning the space resulting from over-sampling.
Moreover, before we run traditional ML we have to handle data to be suitable for the ML technic and maximize F1 score. The technic that use for data preparation for traditional ML is shown below the table.
![deepleaning (4)](https://user-images.githubusercontent.com/107410157/189487745-515b2efb-e43f-48c6-b2b5-fb31796f9d82.png)



# Traditional ML:
We selected 4 traditional ML are HistGradientBoosting, Decision Tree, K-Nearest Neighbors(KNN), and Logistic Regression for Binary classification.
KNN show the higest F1-score 0.9877 and use only 0.02 sec for training and the other technic show performance result as table.

![image](https://user-images.githubusercontent.com/107410157/189485680-2a6b702b-2799-4b5b-98da-5b122ced2b53.png)


# MLP Network architecture:
About MLP, first, we have a review hyperparameter set up with related work, and next step we have trial and error with an increasing number of the hidden layer, number of nodes, number of Epoch, fine-tune Activation function, and dropout rate while fixing Activation function in the output layer, Loss function, type of the optimizer, learning rate, batch size, and validation split as below table.

![deepleaning (1)](https://user-images.githubusercontent.com/107410157/189487379-37527650-3d31-4214-8f6d-febaff90576d.png)

![deepleaning (2)](https://user-images.githubusercontent.com/107410157/189487383-d8bd4bc5-3cb6-4ff6-9744-43287cf01372.png)

We have a trial with 50 combinations and the Top 10 combinations that show the higest accuracy as table.

![deepleaning (3)](https://user-images.githubusercontent.com/107410157/189487781-aa71219d-3ad5-4bad-a4e5-7fe5f667cd8f.png)




# Training:

We selected the best one from MLP run 5 times and the performance of F1-score avg. 0.9523 +/- 0.0011, runtime is 1,266 sec.

![deepleaning](https://user-images.githubusercontent.com/107410157/189488737-3cbc52c5-11dc-4e85-9b49-0a6aea944edd.png)





# Results:
The comparison performance between KNN (the best one of traditional ML) and MLP show that KNN is higher F1-Score and utilize runtime less than MLP

![deepleaning (1)](https://user-images.githubusercontent.com/107410157/189489064-b10ca4a8-abe0-479d-8a6a-7497ff2f447a.png)


# Discussion: 

# Conclusion:
Summarize the results of this homework.
Adjusting Hyperparameter between Traditonal ML and MLP
- Adjusting the Hyperparameter of MLP is more diverse and complex than traditional ML. Hyperparameter is more difficult, as most of the MLP research teams did not provide clear principles for defining the Network architecture, but using the Trial and Error principle, the team decided to use the Trial and Error method, so the results of the MLP could still be improved.
Time and Resources to Build the Model Between Traditional ML and MLP
- Due to the team using Trial and Error principles, it takes much more time and resources to build Model MLP (Extremely) Traditional ML, even though the data is small and tabular. Therefore, tasks that are not complicated should use Traditional ML. More than an MLP

# References:


# Member:


# End credit: 
This project is a part of Course DADS7202 Deep Learning, Data Analytics and Data Science, NIDA.


