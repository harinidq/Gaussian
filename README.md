# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Import the numpy module to use the built-in functions for calculation.
2. Import the sys module to use the built in functions.
3. Get input from the user for number of rows and add it by 1 for number of columns.
4. Using np.zeros() set the matrix as null marix.
5. Using for loop get input from the user for each element in the matrix.
6. Using for loop we can perform the elementary row operations and find the final matrix.
7. Print the values by solving the matrix using for loop with 2 point precision.
8. End the program.

## Program:
```
Program to solve a matrix using Gaussian elimination with partial pivoting.
Developed by: harini.m.d
RegisterNumber: 22001980

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1)) 
x=np.zeros(n)
for i in range(n):
    for j in range (n+1):
        a[i][j]=float(input())
    #print(a)
for i in range(n):
    if a[i][j]==0.0:
        sys. exit('Divide by zero found!')
        
    for j in range(i+1,n):
        scalar=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]-scalar*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2, -1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
        
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ') 
```

## Output:
![Screenshot from 2022-09-24 14-26-20](https://user-images.githubusercontent.com/113497680/192089495-05588482-fd3d-473b-b87b-640cab0726ce.png)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

