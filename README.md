# 🧩 Sudoku Solver in Python

A simple and efficient backtracking-based Sudoku solver implemented in Python.

## 📝 Description

This project solves any valid 9x9 Sudoku puzzle using recursive backtracking. Empty cells are represented by `0`, and the algorithm attempts to fill the board by trying all possibilities while obeying Sudoku rules:

- Each number from 1–9 must appear **once** in each row
- Each number from 1–9 must appear **once** in each column
- Each number from 1–9 must appear **once** in each 3x3 sub-grid

## 📌 Features

- Solves any standard 9x9 Sudoku puzzle
- Backtracking ensures all possible configurations are checked
- Easy to read and modify
- Terminal output for before/after puzzle state

## 🛠 How It Works

1. Find an empty cell (represented by 0)
2. Try placing numbers 1 through 9
3. Validate if placing a number is allowed (row, column, box rules)
4. Recursively proceed to the next cell
5. Backtrack if the configuration becomes invalid

## ▶️ Example Usage

Here's a sample Sudoku puzzle being solved:

```python
# 0s represent empty cells
sudoku_board = [
    [5, 3, 0, 0, 7, 0, 0, 0, 0],
    [6, 0, 0, 1, 9, 5, 0, 0, 0],
    ...
]

if solve_sudoku(sudoku_board):
    print("Sudoku puzzle solved:")
    print_board(sudoku_board)
else:
    print("No solution exists.")
