# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
```
1.Import pandas library to read csv or excel file.
2.Import LabelEncoder using sklearn.preprocessing library.
3.Transform the data's using LabelEncoder.
4.Import decision tree classifier from sklearn.tree library to predict 5.5.the values.
6.Find accuracy.
7.Predict the values.
8.End of the program.
```

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: RAKSHITHA DEVI J
RegisterNumber:212221230082 
*/
```
```
mport pandas as pd
data=pd.read_csv("Employee.csv")
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x=data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```

## Output:
![image](https://user-images.githubusercontent.com/94165326/169459552-bbc60e5c-d87a-414c-a593-86c1850f89eb.png)
![image](https://user-images.githubusercontent.com/94165326/169459583-388dfdb9-d8d1-4747-bde5-8d3949ea295b.png)
![image](https://user-images.githubusercontent.com/94165326/169459624-e3836335-c5aa-4a72-806e-9998d75f9ecf.png)
![image](https://user-images.githubusercontent.com/94165326/169459675-1446d4c9-8806-4948-8860-a1117c9257e9.png)
![image](https://user-images.githubusercontent.com/94165326/169459730-f3293925-067c-4822-bd75-fed5d5f410ce.png)
![image](https://user-images.githubusercontent.com/94165326/169459769-412c0b30-0231-4738-880e-f9a4170c22cd.png)
## without entropy:
![image](https://user-images.githubusercontent.com/94165326/169459806-ad106304-3ca3-4f64-b3b3-c3cb8846ac67.png)
![image](https://user-images.githubusercontent.com/94165326/169459841-1cc66fb5-190c-4187-8c4c-e866182da400.png)
## with entropy:
![image](https://user-images.githubusercontent.com/94165326/169459864-3054f489-a343-452d-8f40-8ef0858a2223.png)
![image](https://user-images.githubusercontent.com/94165326/169459903-e1a53aeb-d64e-4f4c-a7b2-aa82fa614476.png)






## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
