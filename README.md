# Personal Expense Tracker

A command-line Personal Expense Tracker written in Python. It lets you record daily expenses, organise them by category, generate spending reports, view charts, and keep your data between sessions by saving it to a CSV file.

Built as the Major Project for the Artificial Intelligence course by **Irine Micheal**.

## Features

- **Add an expense**: amount, category (chosen from a numbered list) and date (`YYYY-MM-DD`, or press Enter for today)
- **View all expenses** as a formatted table
- **Generate a report**: total spent, average expense, highest expense, spending by category, and total spending by month
- **Charts (Matplotlib)**: bar and pie chart by category, and a bar chart of monthly totals
- **Delete an expense** by number
- **Monthly budget warning**: set a budget once (it is saved) and get a warning at 80% of the budget and when it is exceeded
- **Saved data**: expenses are stored in `expenses.csv` and loaded automatically when the program starts
- **Input validation**: invalid numbers, dates and menu choices are handled with `try-except`, so the program does not crash

## Requirements

- Python 3.8 or later
- Matplotlib

```
python -m pip install matplotlib
```

## How to Run

1. Download or clone this repository.
2. Open a terminal in the project folder.
3. Run:

```
python expense_tracker.py
```

## Menu

```
1. Add an Expense
2. View All Expenses
3. Generate Report
4. Show Category Chart
5. Show Monthly Chart
6. Delete an Expense
7. Set Monthly Budget
8. Save and Exit
```

Choose option **8** to save your expenses before closing. Closing the program any other way will not save new expenses.

## Example Output

```
Date        Category            Amount
--------------------------------------
2026-09-28  Food            $   100.00
2026-09-28  Transport       $    20.00
2026-09-28  Entertainment   $   500.00
2026-09-28  Food            $   150.00
2026-08-12  Bills           $  2000.00
```

```
--- Expense Report ---
Total spent:     $2770.00
Average expense: $554.00
Highest expense: $2000.00 (Bills, 2026-08-12)

Spending by category:
  Food           $   250.00
  Transport      $    20.00
  Entertainment  $   500.00
  Bills          $  2000.00

Spending by month:
  2026-08        $  2000.00
  2026-09        $   770.00
```

## Files

| File | Purpose |
|------|---------|
| `expense_tracker.py` | The main program |
| `expenses.csv` | Saved expenses (created automatically on first save) |
| `budget.txt` | Saved monthly budget (created when a budget is set) |

## Concepts Used

- Lists and dictionaries (each expense is a dictionary stored in a list)
- Functions to keep each operation separate and readable
- Control flow: `if / elif / else`, `while` and `for` loops
- File handling with Python's `csv` module
- Error and exception handling with `try-except`
- Data visualisation with Matplotlib
