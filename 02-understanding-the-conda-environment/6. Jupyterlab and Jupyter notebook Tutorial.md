# JupyterLab and Jupyter Notebook Tutorial

Jupyter is one of the most commonly used tools for:

* Data Science
* Data Analysis
* Machine Learning
* Exploratory Data Analysis
* Python learning

It allows us to combine:

* Code
* Output
* Text
* Charts
* Mathematical equations

inside one document.

---

# What is a Jupyter Notebook?

A Jupyter Notebook is an interactive document stored with the extension:

```text
.ipynb
```

Example:

```text
data-analysis.ipynb
```

A notebook contains multiple **cells**.

---

# Types of Cells

The two most commonly used cells are:

## 1. Code Cell

Used to write and execute Python code.

Example:

```python
print("Hello Data Science")
```

Output:

```text
Hello Data Science
```

---

## 2. Markdown Cell

Used for:

* Headings
* Explanations
* Notes
* Documentation

Example:

```markdown
# Data Analysis

This notebook explores a sales dataset.
```

---

# Starting Jupyter Notebook

Activate your Conda environment:

```bash
conda activate datascience
```

Then run:

```bash
jupyter notebook
```

Jupyter opens in your browser.

---

# Starting JupyterLab

Run:

```bash
jupyter lab
```

This launches the JupyterLab interface.

---

# Creating a Notebook

In Jupyter Notebook:

```text
New
 ↓
Python Kernel
```

In JupyterLab:

```text
Launcher
   ↓
Notebook
   ↓
Python
```

---

# Running a Cell

Write:

```python
a = 10
b = 20

a + b
```

Then press:

```text
Shift + Enter
```

Output:

```text
30
```

---

# Important Keyboard Shortcuts

## Run Cell

```text
Shift + Enter
```

Runs the current cell and moves to the next cell.

## Run Cell Without Moving

```text
Ctrl + Enter
```

## Insert Cell Below

In command mode:

```text
B
```

## Insert Cell Above

```text
A
```

## Delete Cell

```text
D D
```

Press `D` twice.

## Change to Markdown

```text
M
```

## Change to Code

```text
Y
```

---

# Command Mode vs Edit Mode

Jupyter has two important modes.

## Edit Mode

Used when typing inside a cell.

Usually indicated when the cursor is inside the cell.

Press:

```text
Enter
```

to enter Edit Mode.

---

## Command Mode

Used to manage cells.

Press:

```text
Esc
```

to enter Command Mode.

Keyboard shortcuts like:

```text
A
B
M
Y
D D
```

work in Command Mode.

---

# Example Notebook

## Markdown Cell

```markdown
# Basic Python Analysis
```

## Code Cell

```python
numbers = [10, 20, 30, 40, 50]

sum(numbers)
```

Output:

```text
150
```

---

# Using Libraries

Example:

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

---

# Simple Pandas Example

```python
import pandas as pd

data = {
    "Name": ["Aryan", "Rahul", "Aman"],
    "Marks": [85, 78, 91]
}

df = pd.DataFrame(data)

df
```

The DataFrame is displayed as a table directly inside the notebook.

---

# Simple Visualization

```python
import matplotlib.pyplot as plt

marks = [85, 78, 91]
names = ["Aryan", "Rahul", "Aman"]

plt.bar(names, marks)
plt.show()
```

The graph appears directly below the code cell.

---

# Restarting the Kernel

The **kernel** is the process that executes our Python code.

Sometimes variables or libraries cause issues.

We can restart it using:

```text
Kernel → Restart
```

After restarting, all variables stored in memory are removed.

---

# What Does "Run All" Mean?

We can run every notebook cell sequentially using:

```text
Run → Run All Cells
```

This is useful when verifying whether the complete notebook works correctly from beginning to end.

---

# Saving a Notebook

Use:

```text
Ctrl + S
```

or on macOS:

```text
Command + S
```

The notebook is saved as an `.ipynb` file.

---

# Jupyter Notebook vs JupyterLab

| Feature           | Jupyter Notebook | JupyterLab     |
| ----------------- | ---------------- | -------------- |
| Interface         | Simple           | Advanced       |
| Beginner-friendly | Very good        | Good           |
| Multiple files    | Limited          | Excellent      |
| Tabs              | Limited          | Yes            |
| Terminal          | No/limited       | Integrated     |
| File browser      | Basic            | Advanced       |
| Best for          | Learning         | Full workflows |

---

# Jupyter Notebook

Best when:

* Learning Python
* Following tutorials
* Running simple experiments
* Doing basic Data Analysis

---

# JupyterLab

Best when:

* Working on larger Data Science projects
* Managing multiple notebooks
* Using terminals and files together
* Working with multiple datasets

---

# Typical Data Science Workflow

```text
Launch Jupyter
      ↓
Import Libraries
      ↓
Load Dataset
      ↓
Inspect Data
      ↓
Clean Data
      ↓
Perform EDA
      ↓
Visualize Results
      ↓
Build Model
      ↓
Document Findings
```

---

# Useful Commands

Start Notebook:

```bash
jupyter notebook
```

Start JupyterLab:

```bash
jupyter lab
```

Check installed Jupyter packages:

```bash
conda list jupyter
```

Install Jupyter if required:

```bash
conda install jupyter
```

---

# Key Takeaway

Jupyter Notebook provides a simple interactive environment for combining **Python code, explanations, outputs, and visualizations**.

JupyterLab provides the same notebook functionality but adds a more powerful workspace with:

* File management
* Multiple tabs
* Terminals
* Multiple notebooks

For learning, Jupyter Notebook is very easy to start with. For larger Data Science workflows, **JupyterLab is usually more convenient**.
