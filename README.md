##AIM:
To write a program to implement the linear regression using gradient descent.

##Equipments Required:
Hardware – PCs
Anaconda – Python 3.7 Installation / Moodle-Code Runner
##Algorithm:
Use the standard libraries in python for Gradient Design.
Upload the dataset and check any null value using .isnull() function.
Declare the default values for linear regression.
Calculate the loss usinng Mean Square Error.
Predict the value of y.
Plot the graph respect to hours and scores using scatter plot function.
##Program:
/*
Program to implement the linear regression using gradient descent.
Developed by: GANESH P
RegisterNumber:  212220040112
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("student_scores.csv")
data.head()
data.isnull().sum()
x = data.Hours
x.head()
y = data.Scores
y.head()
n = len(x)
m = 0
c = 0
L = 0.001
loss = []
for i in range(10000):
    ypred = m*x + c
    MSE = (1/n) * sum((ypred - y)*2)
    dm = (2/n) * sum(x*(ypred-y))
    dc = (2/n) * sum(ypred-y)
    c = c-L*dc
    m = m-L*dm
    loss.append(MSE)
    #print(m)
print(m,c)
y_pred = m*x + c
plt.scatter(x,y,color = "red")
plt.plot(x,y_pred)
plt.xlabel("Study hours")
plt.ylabel("Scores")
plt.title("Study hours vs. Scores")
plt.plot(loss)
plt.xlabel("Iterations")
plt.ylabel("loss")
*/
##OUTPUT:![output-1](https://user-images.githubusercontent.com/105532515/169082450-c142d2c5-fb47-4bdd-9767-4029e31829f1.png)\n
![output-2](https://user-images.githubusercontent.com/105532515/169082501-eb30761c-ddb7-454d-a5d8-34b7e5eb1dd6.png)


##Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming
