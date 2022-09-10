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
![deepleaning (4)](https://user-images.githubusercontent.com/107410157/189487745-515b2efb-e43f-48c6-b2b5-fb31796f9d82.png)



# Traditional ML:
We selected 4 traditional ML are HistGradientBoosting, Dicision Tree, K-Nearest Neighbors(KNN), Logistic Regression for Binary classification.
KNN show higest F1-score 0.9877 and use only 0.02 sec for training and the other technic show performance result as table.

![image](https://user-images.githubusercontent.com/107410157/189485680-2a6b702b-2799-4b5b-98da-5b122ced2b53.png)


# MLP Network architecture:
About MLP, first we have review hyperparameter set up with related worked and next step we have trial and error with increase number of hidden layer, number of node, number of Epoch, fine-tune Activation function and dropout rate while fix Activation function in output layer, Loss function, type of the optimizer, learning rate, batch size and validation split as below table.

![deepleaning (1)](https://user-images.githubusercontent.com/107410157/189487379-37527650-3d31-4214-8f6d-febaff90576d.png)

![deepleaning (2)](https://user-images.githubusercontent.com/107410157/189487383-d8bd4bc5-3cb6-4ff6-9744-43287cf01372.png)

ทททททททททททททท type of the optimizer, learning rate, batch size and validation split as below table.

![deepleaning (3)](https://user-images.githubusercontent.com/107410157/189487781-aa71219d-3ad5-4bad-a4e5-7fe5f667cd8f.png)


# Training:

MLP with 5 iteration show F1-score 0.9523 +/- 0.0011




# Results:



# Discussion: 

# Conclusion:
สรุปผลของการบ้านครั้งนี้
การปรับ Hyperparameter ระหว่าง Traditonal ML และ MLP
- การปรับ Hyperparameter ของ MLP มีความหลากหลายและซับซ้อนมากกว่า Traditional ML อีกทั้งการอธิบายวิธีการปรับ Hyperparmeter ทำได้ยากกว่า เนื่องจากทีมลองค้นคว้างานลักษณะ MLP ส่วนใหญ่ไม่ได้บอกหลักการกำหนด Netwrok architecture ที่ชัดเจน แต่ใช้หลักการ Trial and Error ทำให้ทีมตัดสินใจเลือกวิธี Trial and Error ดังนั้นผลลัพธ์ของ MLP ยังสามารถพัฒนาปรับปรุงต่อได้
ระยะเวลาและทรัพยากรระหว่างการ Build Model Traditonal ML และ MLP
- สืบเนื่องจากทีมใช้หลักการ Trial and Error ทำให้ต้องใช้ระยะเวลาและทรัพยากรในการ Build Model MLP มากกว่าค่อนข้างมาก (Extreamly) Traditional ML ทั้งๆ ที่ข้อมูลมีขนาดเล็กและมีลักษณะเป็น Tabular ดังนั้นงานที่มีลักษณะไม่ซับซ้อน ควรใช้ Traditional ML มากกว่า MLP

# References:


# Member:


# End credit: 
This project is a part of Course DADS7202 Deep Learning, Data Analytics and Data Science, NIDA.


