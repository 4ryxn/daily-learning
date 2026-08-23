# Loops in Python

Loops are used to **repeat a block of code multiple times**.

According to the Python Refresher, Python has two main types of loops:

```text
for loop
while loop
```

---

# 1. `for` Loop

A `for` loop is used to iterate over sequences such as:

* Lists
* Tuples
* Strings

## Basic Syntax

```python
for variable in sequence:
    # code
```

---

## Example with a List

```python
fruits = ["apple", "banana", "cherry"]

for fruit in fruits:
    print(fruit)
```

Output:

```text
apple
banana
cherry
```

This is the same type of example shown in the refresher.

---

# How a `for` Loop Works

```text
List
 ↓
Take first item
 ↓
Run code
 ↓
Take next item
 ↓
Run code
 ↓
Continue until list ends
```

Example:

```python
numbers = [10, 20, 30]

for number in numbers:
    print(number)
```

Output:

```text
10
20
30
```

---

# Looping Through a String

A string is a sequence of characters, so we can loop through it.

```python
for letter in "Python":
    print(letter)
```

Output:

```text
P
y
t
h
o
n
```

---

# Using `range()`

The refresher also introduces `range()` with loops.

Example:

```python
for i in range(3):
    print(i)
```

Output:

```text
0
1
2
```

Notice that:

```python
range(3)
```

produces values starting from `0` and stops before `3`.

---

# `range(start, stop)`

We can provide a starting point.

```python
for i in range(1, 5):
    print(i)
```

Output:

```text
1
2
3
4
```

The `stop` value is not included.

---

# `range(start, stop, step)`

We can also control the step size.

```python
for i in range(0, 10, 2):
    print(i)
```

Output:

```text
0
2
4
6
8
```

Here:

```text
0  → start
10 → stop
2  → step
```

---

# 2. `while` Loop

A `while` loop keeps running **as long as its condition remains `True`**.

## Basic Syntax

```python
while condition:
    # code
```

---

## Example

```python
count = 0

while count < 3:
    print(count)
    count += 1
```

Output:

```text
0
1
2
```

## The refresher uses this same `count < 3` example.

# How a `while` Loop Works

```text
Check Condition
      ↓
   True?
   /   \
 Yes    No
 ↓       ↓
Run     Stop
Code
 ↓
Check Again
```

Example:

```python
number = 1

while number <= 5:
    print(number)
    number += 1
```

Output:

```text
1
2
3
4
5
```

---

# Important: Update the Condition

Consider:

```python
count = 0

while count < 5:
    print(count)
```

Here, `count` never changes.

So:

```text
count < 5
```

will always remain `True`.

This creates an **infinite loop**.

Correct version:

```python
count = 0

while count < 5:
    print(count)
    count += 1
```

---

# `for` Loop vs `while` Loop

| `for` Loop                               | `while` Loop                                  |
| ---------------------------------------- | --------------------------------------------- |
| Iterates over a sequence                 | Runs while a condition is true                |
| Useful when iterating through items      | Useful when repetition depends on a condition |
| Common with lists, strings and `range()` | Requires careful condition updates            |

---

# 3. Loop Control Statements

The refresher introduces three loop control statements:

```text
break
continue
pass
```

It defines them as:

* `break` → exits the loop
* `continue` → skips to the next iteration
* `pass` → does nothing and can be used as a placeholder

---

# `break`

`break` immediately exits the loop.

Example from the refresher:

```python
for i in range(5):
    if i == 3:
        break

    print(i)
```

Output:

```text
0
1
2
```

When:

```python
i == 3
```

Python executes:

```python
break
```

and stops the loop.

---

# `continue`

`continue` skips the current iteration and moves to the next one.

Example:

```python
for i in range(5):
    if i == 2:
        continue

    print(i)
```

Output:

```text
0
1
3
4
```

When `i` becomes `2`, that iteration is skipped.

---

# `break` vs `continue`

```text
break
  ↓
Stop the complete loop
```

```text
continue
  ↓
Skip current iteration
  ↓
Continue with next iteration
```

---

# `pass`

`pass` does nothing.

It is generally used as a **placeholder** when Python requires a block of code but we do not want to write its implementation yet.

Example:

```python
for i in range(5):
    if i == 2:
        pass

    print(i)
```

Output:

```text
0
1
2
3
4
```

`pass` does not stop or skip the loop.

The refresher defines it specifically as doing nothing and being useful as a placeholder.

---

# Nested Loops

A loop can also exist inside another loop.

Example:

```python
for i in range(2):
    for j in range(3):
        print(i, j)
```

Output:

```text
0 0
0 1
0 2
1 0
1 1
1 2
```

The refresher later also uses this pattern in a nested-loop list comprehension example.

---

# Example: Print Even Numbers

```python
for number in range(10):
    if number % 2 == 0:
        print(number)
```

Output:

```text
0
2
4
6
8
```

This combines:

```text
for loop
+
range()
+
if condition
+
modulus operator
```

---

# Example: Sum of Numbers

```python
total = 0

for number in range(1, 6):
    total += number

print(total)
```

Output:

```text
15
```

Flow:

```text
1 + 2 + 3 + 4 + 5 = 15
```

---

# Quick Revision

## `for` Loop

```python
for item in sequence:
    code
```

## With `range()`

```python
for i in range(5):
    code
```

## `while` Loop

```python
while condition:
    code
```

## `break`

```python
break
```

Stops the loop.

## `continue`

```python
continue
```

Skips the current iteration.

## `pass`

```python
pass
```

Does nothing; works as a placeholder.

---

# Simple Flow

```text
Loops in Python
      |
      ├── for
      |    ├── Lists
      |    ├── Tuples
      |    ├── Strings
      |    └── range()
      |
      └── while
           └── Runs while condition is True

Loop Controls
      |
      ├── break    → Stop
      ├── continue → Skip iteration
      └── pass     → Do nothing
```

---

# Key Takeaways

* Loops allow us to repeat code.
* Python mainly provides `for` and `while` loops.
* `for` loops iterate over sequences.
* `range()` is commonly used with `for` loops.
* `while` loops continue while their condition is `True`.
* `break` stops a loop.
* `continue` skips the current iteration.
* `pass` acts as a placeholder.
