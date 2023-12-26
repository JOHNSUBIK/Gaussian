# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. get the input
2. loop through each row and column
3. use nested loops to perform gaussian elimination
4. prin the result

## Program:
```
Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: John Paul J
RegisterNumber: 23011778
'''
import sys
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    if matrix[i][i]==0.0:
        sys.exit("Divide by zero error")
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
                matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range(n):
    print("X%d = %0.2f"%(i,x[i]),end=' ')
```

## Output:
![Screenshot 2023-12-23 142020](https://github.com/JOHNSUBIK/Gaussian/assets/150279319/79cf2d0a-f14f-464c-801d-f1f0e1d34e44)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

