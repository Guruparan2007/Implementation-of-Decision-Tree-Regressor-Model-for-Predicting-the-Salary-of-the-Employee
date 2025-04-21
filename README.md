# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1. Import pandas

2. Import Decision tree classifier

3. Fit the data in the model

4. Find the accuracy score


## Program:

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

~~~
import pandas as pd
data=pd.read_csv(r"C:\Users\admin\Downloads\Salary.csv")

data.head()
data.info()
data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
print(data.head())

x=data[["Position","Level"]]
print(x.head())

y=data["Salary"]
y.head()

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
print(y_pred)

from sklearn import metrics
r2=metrics.r2_score(y_test,y_pred)
print(r2)

dt.predict([[5,6]])
~~~
~~~
Developed by: GURUPARAN G
RegisterNumber: 212224220030
~~~

## Output:

![Screenshot 2025-04-21 030008](https://github.com/user-attachments/assets/669b5ba6-e227-4147-b8e8-26312a622f4b)

![Screenshot 2025-04-21 030034](https://github.com/user-attachments/assets/f8545953-9a7e-451f-acf5-0212dd292d26)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
