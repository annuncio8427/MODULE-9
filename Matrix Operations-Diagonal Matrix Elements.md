# Matrix Operations-Diagonal Matrix Elements Printer 🧮

This Python program reads a matrix of any size from the user and prints **only the diagonal elements**, leaving other elements blank in the output.

## 📌 Aim

To write a Python program that prints only the diagonal elements of a given matrix.

## 🧠 Algorithm

1. Read the number of rows and columns from the user.
2. Initialize an empty matrix of size `rows × columns`.
3. Populate the matrix with user input.
4. Display the full matrix.
5. Iterate through the matrix and:
   - If `i == j`, print the element (main diagonal).
   - Else, print a blank space.
6. Print a newline after each row.

## 🖥️ Program

rows = int(input())
cols = int(input())

matrix = []
for _ in range(rows):
    row = list(map(int, input().split()))
    matrix.append(row)

for row in matrix:
    print(*row)

for i in range(rows):
    for j in range(cols):
        if i == j:
            print(matrix[i][j], end=' ')
        else:
            print('  ', end=' ')
    print()


### Output:

Enter number of rows: 3
Enter number of columns: 3
Enter the elements row-wise:
1 2 3
4 5 6
7 8 9

Full Matrix:
1 2 3
4 5 6
7 8 9

Diagonal Elements Matrix:
1      
    5   
       9 

## Result

The program successfully reads a 3×3 matrix from the user and displays:

The full matrix as entered:

1 2 3
4 5 6
7 8 9


Only the diagonal elements of the matrix, leaving other positions blank to maintain the matrix shape:

1      
  5    
    9  


This output clearly highlights the main diagonal elements of the matrix, fulfilling the program’s aim. The spaces ensure that the diagonal elements stay aligned with their original positions.
