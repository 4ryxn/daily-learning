   # If-Else and Functions in Python

# 1. If-Else Conditions

Conditional statements allow a Python program to **make decisions based on conditions**.

Python mainly uses:

```text
if
if-else
if-elif-else
```

They are useful in Data Science for tasks such as:

* Filtering data
* Categorizing values
* Data cleaning
* Applying business rules
* Decision-making

---

## Basic `if` Statement

The `if` statement executes a block of code only when its condition is `True`.

### Syntax

```python
if condition:
    # code to execute
```

### Example

```python
x = 10

if x > 5:
    print("x is greater than 5")
```

Output:

```text
x is greater than 5
```

Python checks:

```text
x > 5
  ↓
True
  ↓
Execute the if block
```

If the condition is `False`, the block is skipped.

---

# `if-else` Statement

The `else` block executes when the `if` condition is `False`.

### Syntax

```python
if condition:
    # if condition is True
else:
    # if condition is False
```

### Example

```python
x = 3

if x > 5:
    print("x is greater than 5")
else:
    print("x is not greater than 5")
```

Output:

```text
x is not greater than 5
```

---

# `if-elif-else` Statement

When multiple conditions need to be checked, use `elif`.

`elif` means:

```text
else if
```

### Syntax

```python
if condition1:
    # code
elif condition2:
    # code
else:
    # code
```

### Example

```python
x = 5

if x > 10:
    print("x is greater than 10")
elif x > 5:
    print("x is greater than 5 but not more than 10")
elif x == 5:
    print("x is exactly 5")
else:
    print("x is less than 5")
```

Output:

```text
x is exactly 5
```

Python checks conditions **from top to bottom**.

The first `True` condition executes and the remaining conditions are skipped.

---

# Example: Categorizing Data

```python
age = 25

if age < 18:
    category = "Minor"
elif age < 65:
    category = "Adult"
else:
    category = "Senior Citizen"

print("Category:", category)
```

Output:

```text
Category: Adult
```

This is useful when numerical data needs to be converted into categories.

---

# Indentation

Indentation is very important in Python.

Correct:

```python
age = 20

if age >= 18:
    print("Adult")
```

Incorrect:

```python
age = 20

if age >= 18:
print("Adult")
```

Python uses indentation to determine which statements belong to a block.

---

# Using Logical Operators with Conditions

Conditions can be combined using:

```text
and
or
not
```

## `and`

Both conditions must be true.

```python
age = 25

if age >= 18 and age < 60:
    print("Eligible")
```

---

## `or`

At least one condition must be true.

```python
day = "Sunday"

if day == "Saturday" or day == "Sunday":
    print("Weekend")
```

---

## `not`

Reverses the condition.

```python
is_raining = False

if not is_raining:
    print("You can go outside")
```

---

# 2. Functions in Python

A **function** is a reusable block of code designed to perform a particular task.

Instead of writing the same code repeatedly, we can put it inside a function and call it whenever required.

Basic structure:

```python
def function_name():
    # code
```

---

# Creating a Function

Python uses the `def` keyword to define a regular function.

```python
def greet():
    print("Hello!")
```

Here:

* `def` → defines the function
* `greet` → function name
* `()` → contains parameters if required
* `:` → starts the function body

---

# Calling a Function

Defining a function does not automatically execute it.

We call it using its name:

```python
def greet():
    print("Hello!")

greet()
```

Output:

```text
Hello!
```

---

# Function with Parameters

A function can receive information through **parameters**.

```python
def greet(name):
    print("Hello", name)

greet("Alice")
```

Output:

```text
Hello Alice
```

Here:

```text
name → Parameter
"Alice" → Argument
```

### Parameter vs Argument

* **Parameter:** Variable written in the function definition.
* **Argument:** Actual value passed when calling the function.

---

# Function with Multiple Parameters

```python
def add(a, b):
    print(a + b)

add(10, 20)
```

Output:

```text
30
```

---

# Returning a Value

A function can send a result back using `return`.

```python
def add(a, b):
    return a + b

result = add(10, 20)

print(result)
```

Output:

```text
30
```

Think of it as:

```text
Input
  ↓
Function
  ↓
Processing
  ↓
return
  ↓
Output
```

---

# `print()` vs `return`

These are different.

### Using `print()`

```python
def add(a, b):
    print(a + b)
```

This only displays the result.

### Using `return`

```python
def add(a, b):
    return a + b
```

This gives the result back so it can be stored or used later.

Example:

```python
result = add(5, 10)

print(result * 2)
```

Output:

```text
30
```

---

# Function with If-Else

Functions and conditional statements are often used together.

```python
def check_number(number):

    if number > 0:
        return "Positive"

    elif number < 0:
        return "Negative"

    else:
        return "Zero"
```

Calling it:

```python
print(check_number(10))
```

Output:

```text
Positive
```

---

# Example: Pass or Fail Function

```python
def check_result(score):

    if score >= 50:
        return "Pass"
    else:
        return "Fail"


print(check_result(75))
```

Output:

```text
Pass
```

This shows how functions can contain decision-making logic.

---

# Lambda Functions

Your refresher later introduces **lambda functions**.

A lambda function is an **anonymous, single-expression function** created using the `lambda` keyword. It is mainly useful for short operations where writing a full `def` function is unnecessary.

## Syntax

```python
lambda arguments: expression
```

Example:

```python
square = lambda x: x ** 2

print(square(5))
```

Output:

```text
25
```

---

# Normal Function vs Lambda

Normal function:

```python
def square(x):
    return x ** 2
```

Lambda equivalent:

```python
square = lambda x: x ** 2
```

Both can produce the same result.

---

# Lambda with Multiple Arguments

```python
add = lambda x, y: x + y

print(add(3, 7))
```

Output:

```text
10
```

This multiple-argument lambda example also appears in the refresher.

---

# When to Use Lambda

According to the refresher, lambda functions are useful when:

* The function is short and simple
* It is needed temporarily
* A complete `def` function would be unnecessary

Avoid lambda functions when:

* The logic is complex
* Multiple statements are needed
* A normal function would be easier to read

---

# Quick Revision

## Conditional Statements

```text
if
↓
Run when condition is True

if-else
↓
Choose between two outcomes

if-elif-else
↓
Handle multiple conditions
```

## Functions

```text
def
 ↓
Define Function
 ↓
Parameters / Arguments
 ↓
Execute Code
 ↓
return
 ↓
Result
```

## Basic Function

```python
def function_name(parameter):
    return result
```

## Lambda

```python
lambda arguments: expression
```

---

# Key Takeaways

* `if` executes code when a condition is `True`.
* `else` handles the alternative case.
* `elif` allows multiple conditions to be checked.
* Python checks an `if-elif-else` chain from top to bottom.
* Functions help organize and reuse code.
* `def` is used to define a normal Python function.
* Parameters allow functions to accept input.
* `return` sends a value back from a function.
* Functions can contain `if-else` logic.
* Lambda functions provide a shorter way to write simple single-expression functions.
