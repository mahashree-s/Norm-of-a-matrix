# Norm of a matrix
## Aim
To write a program to find the 1-norm, 2-norm and infinity norm of the matrix and display the result in two decimal places.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
	1. Get the input matrix using np.array()   
    2. Find the 2-norm of the matrix using np.linalg.norm()
	3. Print the norm of the matrix in two decimal places.
## Program:
```Python
# Register No: 212225230163
# Developed By: mahashree s
# 1-Norm of a Matrix
matrix = eval(input())

rows = len(matrix)
cols = len(matrix[0])

max_sum = 0

for j in range(cols):
    col_sum = 0
    for i in range(rows):
        col_sum += abs(matrix[i][j])
    if col_sum > max_sum:
        max_sum = col_sum

print(f"{max_sum:.2f}")



# 2-Norm of a Matrix
'''
Program to find 2-norm of a matrix.
Developed by: mahashree s
RegisterNumber: 212225230163
'''
import os
os.environ["OPENBLAS_NUM_THREADS"]="1"

import numpy as np

matrix = np.array(eval(input()))

l2_norm = np.linalg.norm(matrix, 2)

print(f"{l2_norm:.2f}")



# Infinity Norm of a Matrix
matrix = eval(input())

max_sum = 0

for row in matrix:
    row_sum = 0
    for val in row:
        row_sum += abs(val)
    if row_sum > max_sum:
        max_sum = row_sum

print(f"{max_sum:.2f}")




```
## Output:
### 1-Norm of a Matrix
<br>
<br>
<img width="720" height="279" alt="image" src="https://github.com/user-attachments/assets/3d668a1c-f1ea-49e0-a0a3-1a147cd01f3d" />

<br>

### 2-Norm of a Matrix
<br>
<br>
<img width="671" height="338" alt="image" src="https://github.com/user-attachments/assets/35392e73-4a17-4cd9-9ee0-ea65ad09924a" />

<br>

### Infinity Norm of a Matrix
<br>
<br>
<img width="699" height="302" alt="image" src="https://github.com/user-attachments/assets/b1057554-9e1c-4dcd-b1b6-c38403174d14" />

<br>

## Result
Thus the program for 1-norm, 2-norm and Infinity norm of a matrix are written and verified.
