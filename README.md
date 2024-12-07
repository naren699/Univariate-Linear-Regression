# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
import numpy as np
import matplotlib.pyplot as plt
X= np.array([0,1,2,3,4,5,6,7,8,9])
Y= np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(X,Y)
plt.show()
X_Mean=np.mean(X)
Y_Mean=np.mean(Y)
num=0
den=0
for i in range(len(X)):
    num+=(X[i]-X_Mean)*(Y[i]-Y_Mean)
    den+=(X[i]-X_Mean)**2
m=num/den
b=Y_Mean-(m*X_Mean)
print(m,b)
Y_Pred=(m*X)+b
print(Y_Pred)
plt.scatter(X,Y,color='Red')
plt.plot(X,Y_Pred,color='Blue')
plt.show()


## Input
![Screenshot 2024-12-07 235511](https://github.com/user-attachments/assets/548d25bb-d86d-4d47-900d-8f908b14348b)




## Output
![Screenshot 2024-12-07 235501](https://github.com/user-attachments/assets/e0684c12-6473-4eea-8647-830725c5d8ae)
![Screenshot 2024-12-07 235522](https://github.com/user-attachments/assets/d39c6d92-6368-4132-9c8f-a70ef0074a39)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
