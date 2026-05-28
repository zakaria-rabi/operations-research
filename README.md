# ⚙️ Operations Research

> Linear Programming and optimization exercises — Master IARO, UMI Meknes

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)](https://python.org)
[![PuLP](https://img.shields.io/badge/PuLP-LP%20Solver-blue?style=flat)](https://coin-or.github.io/pulp/)
[![GLPK](https://img.shields.io/badge/GLPK-Optimization-green?style=flat)](https://www.gnu.org/software/glpk/)

---

## 📁 Structure

```
operations-research/
│
├── linear-programming/
│   ├── simplex_method.ipynb
│   ├── transportation_problem.ipynb
│   └── assignment_problem.ipynb
│
├── integer-programming/
│   ├── knapsack_problem.ipynb
│   └── branch_and_bound.ipynb
│
├── metaheuristics/
│   ├── genetic_algorithm.ipynb
│   └── simulated_annealing.ipynb
│
└── solvers/
    ├── pulp_examples.ipynb
    ├── glpk_examples.ipynb
    └── cbc_examples.ipynb
```

---

## 🧪 Topics Covered

| Topic | Method | Solver |
|-------|--------|--------|
| Linear Programming | Simplex, Graphical | PuLP / GLPK |
| Transportation Problem | North-West, Vogel | PuLP |
| Integer Programming | Branch & Bound | CBC |
| Knapsack Problem | Dynamic Programming | Python |
| Metaheuristics | Genetic Algorithm, SA | Python |

---

## 🛠️ Setup

```bash
git clone https://github.com/zakaria-rabi/operations-research.git
cd operations-research
pip install -r requirements.txt
```

**Requirements:**
```
pulp
numpy
pandas
matplotlib
jupyter
```

**Install GLPK (optional):**
```bash
# Ubuntu/Debian
sudo apt-get install glpk-utils

# Windows
# Download from: http://winglpk.sourceforge.net/
```

---

## 💡 Example — Simple LP with PuLP

```python
from pulp import *

# Define problem
prob = LpProblem("Maximize_Profit", LpMaximize)

# Variables
x = LpVariable("x", lowBound=0)
y = LpVariable("y", lowBound=0)

# Objective
prob += 5*x + 4*y

# Constraints
prob += 6*x + 4*y <= 24
prob += x + 2*y <= 6

# Solve
prob.solve()
print(f"x = {value(x)}, y = {value(y)}")
print(f"Profit = {value(prob.objective)}")
```

---

## 👤 Author

**Zakaria Rabi** — Master IARO, Moulay Ismail University  
📧 zakariarabi662@gmail.com | 🐙 [github.com/zakaria-rabi](https://github.com/zakaria-rabi)
