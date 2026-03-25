# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

1. Import the required library (NumPy).

2• Define the coefficient matrix (and constant matrix if solving linear equations).

3• Apply row operations to convert the matrix into upper triangular form (make elements below the main diagonal zero)

4• Display the resulting upper triangular matrix (or perform back substitution to get the solution).

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: HARINARAYANAN.A
RegisterNumber: 212225230090

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][j]==0:
        sys.exit('divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range (n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ') 

```

## Output:

<img width="815" height="775" alt="image" src="https://github.com/user-attachments/assets/5d6b4775-66e1-4955-a738-1e64e63af5a1" />


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

