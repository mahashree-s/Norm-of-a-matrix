# Norm of a matrix
## Aim
To write a program to find the 1-norm, 2-norm and infinity norm of the matrix and display the result in two decimal places.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner

### Algorithm 1: 1-Norm of a Matrix

1. Start.
2. Read the matrix as input.
3. Find the number of rows and columns.
4. Set `max_sum = 0`.
5. For each column:

   * Set `col_sum = 0`.
   * Add the absolute values of all elements in that column.
   * Compare `col_sum` with `max_sum`.
   * Store the larger value in `max_sum`.
6. Print `max_sum` up to two decimal places.
7. Stop.

**Formula:**

$$
\|A\|_1 = \max_j \sum_i |a_{ij}|
$$

---

### Algorithm 2: 2-Norm of a Matrix

1. Start.
2. Read the matrix as input.
3. Convert the matrix into a NumPy array.
4. Calculate the matrix 2-norm using `numpy.linalg.norm(matrix, 2)`.
5. Store the result in `l2_norm`.
6. Print the result up to two decimal places.
7. Stop.

**Formula:**

$$
\|A\|_2 = \sqrt{\lambda_{\max}(A^TA)}
$$


---

### Algorithm 3: Infinity Norm of a Matrix

1. Start.
2. Read the matrix as input.
3. Set `max_sum = 0`.
4. For each row:

   * Set `row_sum = 0`.
   * Add the absolute values of all elements in that row.
   * Compare `row_sum` with `max_sum`.
   * Store the larger value in `max_sum`.
5. Print `max_sum` up to two decimal places.
6. Stop.

**Formula:**

$$
\|A\|_\infty = \max_i \sum_j |a_{ij}|
$$


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
