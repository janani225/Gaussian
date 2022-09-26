# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm:

1.Get the matrix from user.

2.Using "from numpy as np" to import numpy.

3.Using numpy library we solve the matrix using gaussian elimination with partial pivoting.

4.Print the result matrices (Gaussian Elimination).

5.End the program. 

## Program:
```

Program to find the solution of a matrix using Gaussian Elimination.
Developed by: V.S.JANANI
RegisterNumber: 22003192

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
![Screenshot from 2022-09-26 10-20-27](https://user-images.githubusercontent.com/113497333/192196164-ccf684de-f35d-42e6-9224-32a251dc55bf.png)




## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

