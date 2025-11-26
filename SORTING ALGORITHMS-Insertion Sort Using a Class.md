# 🧮 SORTING ALGORITHMS: Insertion Sort Using a Class

This program demonstrates how to implement the **Insertion Sort algorithm** using a Python class. It allows the user to input a list of numbers, sorts them using the insertion sort technique, and displays the sorted list.

---

## 🎯 Aim

To develop a Python class with functions to:
- Create a list of integers
- Sort it using the **Insertion Sort** algorithm
- Display the sorted list

---

## 🧠 Algorithm

1. **Start the program**
2. **Define a class** `InsertionSorter`
3. Inside the class:
   - `create_list()`:
     - Read number of elements
     - Store them in a list
   - `insertion_sort()`:
     - Iterate from the second element to the end
     - Move elements greater than the key to one position ahead
     - Insert the key at the correct position
   - `print_list()`:
     - Print the sorted list
4. **Create an object** of the class
5. **Call** the methods in order: `create_list()`, `insertion_sort()`, and `print_list()`
6. **End the program**

---

## 💻 PROGRAM:

class InsertionSorter:
    def __init__(self):
        self.data = []

    def create_list(self):
        n = int(input())
        self.data = list(map(int, input().split()))
        if len(self.data) != n:
            print(f"Error: Expected {n} elements but got {len(self.data)}.")
            exit(1)

    def insertion_sort(self):
        for i in range(1, len(self.data)):
            key = self.data[i]
            j = i - 1
            while j >= 0 and self.data[j] > key:
                self.data[j + 1] = self.data[j]
                j -= 1
            self.data[j + 1] = key

    def print_list(self):
        print(*self.data)

sorter = InsertionSorter()

sorter.create_list()
sorter.insertion_sort()
sorter.print_list()


## OUTPUT:

5
12 11 13 5 6
5 6 11 12 13

## RESULT:

RESULT:

The program reads a list of integers, sorts them using the insertion sort algorithm implemented inside a class, and prints the sorted list correctly. It successfully demonstrates class usage and the insertion sort logic.
