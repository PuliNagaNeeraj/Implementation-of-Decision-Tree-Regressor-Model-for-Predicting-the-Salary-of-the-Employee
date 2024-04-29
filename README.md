# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree import DecisionTreeClassifier and use criterion as entropy. 
5. Find the accuracy of the model and predict the required values by importing the required module from sklearn.
## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: PULI NAGA NEERAJ
RegisterNumber: 212223240130
```
```
import pandas as pd
data=pd.read_csv("Salary.csv")
data.head()
data.info()
```
```
data.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
```
```
x= data[["Position","Level"]]
y=data["Salary"]
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size = 0.2,random_state = 2)
```
```
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
```
```
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
```
```
r2= metrics.r2_score(y_test,y_pred)
r2
```
```
dt.predict([[5,6]])
```
## Output:

### data.head()
![image](https://github.com/Abburehan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/138849336/302d9fc9-e8e8-4b0f-b300-ac9f1d1f646d)

### data.info()
![image](https://github.com/Abburehan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/138849336/9379e9aa-f8f5-4464-8331-28c7af877859)

### Null dataset
![image](https://github.com/Abburehan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/138849336/5747640c-c4e4-40ca-a8a4-a6f5ffd95c6d)

### Data head after Label Encoder
![image](https://github.com/Abburehan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/138849336/680606f3-7c1d-4144-9fe8-6d7cb222d82a)

### MSE
![image](https://github.com/Abburehan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/138849336/e1723b08-246b-47d2-baa5-95b8ac448635)

### x.head()
![image](https://github.com/Abburehan/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/138849336/4163c72b-82b7-4c0e-8699-27bb8e658e08)

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
