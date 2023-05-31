# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.First,we want to import numpy,then import sys,assume a variable.

2.For gaussian elimination method, we want to make 2nd and 3rd column zero.

3.For that we want to make a range accorting to our program output.

4.Then print the program with correct form then the output will display.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Lokesh N
RegisterNumber:212222100023 
*/
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
X=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0.0:
        sys.exist('Divide by zero found')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
X[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    X[i]=a[i][n]
    for j in range(i+1,n):
        X[i]=X[i]-a[i][j]*X[j]
    X[i]=X[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,X[i]),end=' ')

```

## Output:

![image](https://github.com/lokeshnarayanan/Gaussian/assets/119393019/4e1ccd5f-b508-4d17-a9a2-b549bf672745)


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

