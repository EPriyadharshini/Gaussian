# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.import the sys module to use the built-in function calculation
2,import the sys module to use the built in function
3.get input from the user for number of rows and add it by 1 for number of columns
4.using np.zeros() set the matrix as null matrix
5.using nested for loop get input from the user for each element in the matrix
6.using nested for loop find the ratio and perform the elementary row opeations and find the final matrix.
7.use back substitution method to find the value of the variables and print it.
8.End the program.

## Program:
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by:PRIYADHARSHINI.E
RegisterNumber:23012593
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
         a[i][j] = float(input())
for i in range(n):
    if a[i][j] == 0.0:
        sys.exit('Devide by zero detected!') 
    for j in range(i+1, n):
        ratio = a[j][i]/a[i][i] 
        for k in range(n+1):
            a[j][k] = a[j][k] - ratio * a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1] 
    
for i in range(n-2,-1,-1):
    x[i] = a[i][n]

    for j in range(i+1, n):
           x[i] = x[i] - a[i][j]*x[j]
           
    x[i] = x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]), end = ' ')
 






































## Output:


<img width="276" alt="image" src="https://github.com/EPriyadharshini/Gaussian/assets/144870831/d70f6a15-6b33-436e-9cdd-fc99443f0e10">


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

