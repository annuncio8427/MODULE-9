# ➖ Matrix Operations-Matrix Subtraction in Python

## 🎯 AIM:

To write a Python program that reads two matrices from the user and performs matrix subtraction.

---

## 🧠 ALGORITHM:

1. **Start**
2. Create variables `r` and `c` for rows and columns
3. Get the values of `r` and `c` from the user
4. Define a function `create_matrix(n, m)` to:
   - Prompt user for each matrix element
   - Append each row to form a complete matrix
5. Call the `create_matrix()` function twice to read two matrices `A` and `B`
6. Define a loop to subtract the elements of matrix `B` from matrix `A`
7. Store the result in a new matrix `C`
8. Print the resulting matrix `C`
9. **Stop**

---

## 💻 PROGRAM:

```python
def create_matrix(rows, cols):
    matrix = []
    for _ in range(rows):
        row = list(map(int, input().split()))
        matrix.append(row)
    return matrix

r = int(input())
c = int(input())

A = create_matrix(r, c)
B = create_matrix(r, c)

C = []
for i in range(r):
    row = []
    for j in range(c):
        row.append(A[i][j] - B[i][j])
    C.append(row)

for row in C:
    print(*row)
```

## OUTPUT:

```
3
3
9 8 7
6 5 4
3 2 1
1 2 3
4 5 6
7 8 9

Result:
8 6 4
2 0 -2
-4 -6 -8
```

## RESULT:

The program reads two 3×3 matrices from the user, subtracts the second matrix from the first element-wise, and correctly outputs the resulting matrix. This successfully demonstrates matrix subtraction in Python using nested loops.
