# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. import numpy as np 
2. Initialize the matrix with the given coefficients and constants.
3. For each pivot element, calculate the multipliers for each row below the pivot and subtract the corresponding rows from the current row.
4. Repeat the process for each pivot element in the matrix.
5. If the solution is not correct, repeat the process.
## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Rathish kuamr C
RegisterNumber: 22009283
'''
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
x[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=arr[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-arr[i][j]*x[j]
    x[i]=x[i]/arr[i][i]
*/
```

## Output:

![gaussian](https://user-images.githubusercontent.com/120539398/214771813-d7992f19-d1f2-423f-9d7a-904e2e5182e8.png)

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

