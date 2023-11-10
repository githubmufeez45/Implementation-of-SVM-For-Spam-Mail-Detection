# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages.
2.Read the given csv file and display the few contents of the data.
3.Assign the features for x and y respectively.
4.Split the x and y sets into train and test sets.
5.Convert the Alphabetical data to numeric using CountVectorizer.
6.Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.
7.Find the accuracy of the model.
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: arun.j
RegisterNumber:  212222040015

import chardet
file='/content/spam (1).csv'
with open(file, 'rb') as rawdata:
     print('Result output')
    result = chardet.detect(rawdata.read(10000))
result
import pandas as pd
data=pd.read_csv("/content/spam (1).csv",encoding="windows-1252")
print("Data Head ")
data.head()
print("data info")
data.info()
print("data.isnull()")
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extraction.text import CountVectorizer 
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
print("y_pred")
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
print("accuracy")
accuracy
*/
```

## Output:
# data.head():
![279339861-968d89bc-0906-4928-a115-637da7c115d1](https://github.com/githubmufeez45/Implementation-of-SVM-For-Spam-Mail-Detection/assets/134826568/4d338a89-3890-44c2-bf9f-dd60cb8cff2c)

# data.info():
![279340067-3838a508-d25a-408f-ae70-5ce4155403ee](https://github.com/githubmufeez45/Implementation-of-SVM-For-Spam-Mail-Detection/assets/134826568/77980927-6c34-4763-b7bd-590f9ae26491)

# 3.data.isnull().sum():
![279340159-726443d4-9135-4aeb-b3c6-6d988525e73f](https://github.com/githubmufeez45/Implementation-of-SVM-For-Spam-Mail-Detection/assets/134826568/f2e0d60a-8b40-487e-8236-00bf0506c44d)

# Y_prediction Value:
![279343982-8b76ea17-c8b5-45f2-a312-15744521b4f7](https://github.com/githubmufeez45/Implementation-of-SVM-For-Spam-Mail-Detection/assets/134826568/b404edfa-c895-4281-b38d-3b5085a6b5db)

# Accuracy Value: 
![279344141-9c10b30f-cc21-4146-8134-a19b63ed41f0](https://github.com/githubmufeez45/Implementation-of-SVM-For-Spam-Mail-Detection/assets/134826568/2aa9111e-ca68-46bd-a156-822751e47e2b)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
