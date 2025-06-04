# 🧩 AI Crossword Solver

A Constraint Satisfaction Problem (CSP)-based model for solving crossword puzzles, written in Python. This project generates valid crossword solutions from a grid structure and word list using AI search techniques.

## 🚀 Features

- Parses crossword grid structure and word list files.
- Implements CSP solving techniques:
  - Node Consistency (unary constraint enforcement)
  - Arc Consistency using AC-3 algorithm
  - Backtracking Search with heuristics:
    - MRV (Minimum Remaining Values)
    - Degree Heuristic
    - LCV (Least Constraining Value)
- Visualizes solution in the terminal
- Optionally outputs a `.png` image using the PIL library

---

## 🛠️ Technical Skills Demonstrated

| Category               | Skills & Tools                                               |
|------------------------|--------------------------------------------------------------|
| **Programming**        | Python, OOP, command-line interface                          |
| **AI Concepts**        | Constraint Satisfaction Problems, Backtracking, Inference    |
| **Search Algorithms**  | AC-3, MRV, Degree Heuristic, LCV                             |
| **Libraries Used**     | `PIL` (Python Imaging Library)                               |
| **Software Design**    | Modular, class-based architecture                            |
| **Problem Solving**    | Consistency checks, constraint propagation, search pruning   |

---

## 📁 File Structure
```
crosswords/
├── assets/
│ └── fonts/ # Fonts for rendering image output
├── data/ # Contains structure and word list files
├── crossword.py # Crossword grid and variable definitions
├── generate.py # CrosswordCreator class & solving logic
├── output.png # Example rendered crossword output
└── README.md # Project documentation
```
---

## 📚 Key Concepts Implemented

### 🔹 Node Consistency
Ensures that the domain of each variable contains only values that satisfy the variable’s length constraint.

### 🔹 Arc Consistency (AC-3)
Prunes domain values that are inconsistent with neighboring variables' domains based on overlap constraints.

### 🔹 Backtracking Search
Recursively assigns values to variables, backtracking when inconsistencies arise.

### 🔹 Heuristics
- **MRV (Minimum Remaining Values):** Prioritize variables with the fewest legal values.
- **Degree Heuristic:** Break ties by selecting the variable with the most constraints on other variables.
- **LCV (Least Constraining Value):** Prefer values that eliminate the fewest options for neighboring variables.

---

## 🧪 Example Usage

```bash
python generate.py data/structure.txt data/words.txt output.png
```
This will generate and solve the crossword, print it in the terminal, and save the solution as output.png.