
# Traditional ML vs MLP for Diabetes Binary Classification
## Dataset
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


# Exploratory Data Analysis :
This dataset has 21 feature variables and is not balanced. We have cleansed data by exploring null/duplicate/distribution. 
  - Handle Imbalanced data by using SMOTE which is the method that can generate noisy samples by interpolating new points between marginal outliers and inliers. This issue can be solved by cleaning the space resulting from over-sampling. 
  - Handle Outlier by IQR (Interquartile range)
  - Handle Standardize by StandardScaler

  Moreover, before we run traditional ML we have to handle data to be suitable for the ML technique and maximize F1 score. The technique that use for data preparation for traditional ML is shown below the table.
![deepleaning (4)](https://user-images.githubusercontent.com/107410157/189487745-515b2efb-e43f-48c6-b2b5-fb31796f9d82.png)



# Traditional ML:
We selected 4 traditional ML are HistGradientBoosting, Decision Tree, K-Nearest Neighbors(KNN), and Logistic Regression for Binary classification.
KNN show the higest F1-score 0.9877 and use only 0.02 sec for training and the other technique show performance result as table.

![image](https://user-images.githubusercontent.com/107410157/189485680-2a6b702b-2799-4b5b-98da-5b122ced2b53.png)


# MLP Network architecture:
About MLP, first, we have a review hyperparameter set up with related work, and next step we have trial and error with an increasing number of the hidden layer, number of nodes, number of Epoch, fine-tune Activation function, and dropout rate while fixing Activation function in the output layer, Loss function, type of the optimizer, learning rate, batch size, and validation split as below table.

![deepleaning (1)](https://user-images.githubusercontent.com/107410157/189487379-37527650-3d31-4214-8f6d-febaff90576d.png)

![deepleaning (2)](https://user-images.githubusercontent.com/107410157/189487383-d8bd4bc5-3cb6-4ff6-9744-43287cf01372.png)

We have a trial with 39 combinations and the Top 10 combinations that show the higest accuracy as table.

![deepleaning (3)](https://user-images.githubusercontent.com/107410157/189487781-aa71219d-3ad5-4bad-a4e5-7fe5f667cd8f.png)




# Training:

We selected the best one from MLP run 5 times and the performance of F1-score avg. 0.9523 +/- 0.0011, runtime is 1,266 sec.
Train accuracy vs Train loss show the problem on this training is overfit.

![deepleaning](https://user-images.githubusercontent.com/107410157/189488737-3cbc52c5-11dc-4e85-9b49-0a6aea944edd.png)

![deepleaning (2)](https://user-images.githubusercontent.com/107410157/189490390-09794b8c-483f-46ca-901e-b46e9773c3c4.png)





# Results:
The comparison performance between KNN (the best one of traditional ML) and MLP show that Traditional ML is higher F1-Score than MLP and utilize runtime less than MLP significantly.

![deepleaning (1)](https://user-images.githubusercontent.com/107410157/189489064-b10ca4a8-abe0-479d-8a6a-7497ff2f447a.png)


# Discussion:
1. The imbalance correction increased Accuracy in both Traditional ML and MLP, as expected. In addition, an imbalance with SMOTE_ENN (from imblearn.combine import SMOTEENN) resulted in a more significant increase in Accuracy. Compared to sklearn oversampling (from sklearn.utils import resample).

2. The increasing number of layers does not guarantee that the Accuracy will increase. Because if we set a small number of layers, but if there is a large number of epochs, it can increase the Accuracy.

3. The Epoch number affects the Accuracy, as expected. But if we increase the number of Epoch more and more. Found that it doesn't affect Accuracy, which is unexpected because the team understands that it can keep pushing until the Accuracy reaches 0.99.

4. The number of batch sizes had no significant effect on Accuracy, which was unexpected as the team understood that more batch sizes would increase Accuracy.

6. The higher the learning rate, the lower the default value. This increased the Accuracy, as expected. Initially, the team used default 0.01, then adjusted it to 0.0001.

# Conclusion:
Summarize the results of this homework.

Adjusting Hyperparameter between Traditonal ML and MLP
- Adjusting the Hyperparameter of MLP is more diverse and complex than traditional ML. Hyperparameter is more difficult, as most of the MLP research teams did not provide clear principles for defining the Network architecture, but using the Trial and Error principle, the team decided to use the Trial and Error method, so the results of the MLP could still be improved.

Time and Resources to Build the Model Between Traditional ML and MLP
- Due to the team using Trial and Error principles, it takes much more time and resources to build Model MLP (Extremely) Traditional ML, even though the data is small and tabular. Therefore, tasks that are not complicated should use Traditional ML. More than an MLP

# References:
Basic machine learning
  - youtube chanel: data professor (Associate Professor Chanin Nantasenamat, Ph.D.)
 
Handle outlier
  - https://medium.com/@prashant.nair2050/hands-on-outlier-detection-and-treatment-in-python-using-1-5-iqr-rule-f9ff1961a414
  - https://www.analyticsvidhya.com/blog/2021/05/feature-engineering-how-to-detect-and-remove-outliers-with-python-code/

AE-MLP
  - A Hybrid Deep Learning Approach for DDoS Detection and Classification, Yuanyuan Wei; Julian Jang-Jaccard; Fariza Sabrina; Amardeep Singh; Wen Xu; Seyit Camtepe, IEEE Access (Volume: 9), Page(s): 146810 - 146821, 27 October 2021

Reference version
![deepleaning](https://user-images.githubusercontent.com/86920208/189493303-c8e845e1-ed8c-4461-996f-120a14d1031a.jpg)

# Member:
1.(20%) Athit Santikarn 6410414007
- Research / Train and tune ML / Write result, discussion, conclusion report

2.(20%) Suphanun Sukamta 6410422020
- Research / Train and tune ML / Write result, discussion, conclusion report

3.(20%) Chokchai Kenpho 6410422004
- Prepare and clean dataset / Train and tune ML & MLP model / Write network architecture, training, discussion, conclusion report

4.(20%) Noppol Anakpluek 641422009
- Prepare and clean dataset / Train and tune ML & MLP model / Write network architecture, training, discussion, conclusion report

5.(20%) Watcharakorn Pasanta 6420422006
- Prepare and clean dataset / Train and tune ML & MLP model / Write network architecture, training, discussion, conclusion report

# End credit: 
This project is a part of Course DADS7202 Deep Learning, Data Analytics and Data Science, NIDA.


