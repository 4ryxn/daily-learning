# Operator Precedence in Python

Operator precedence defines the **order in which Python evaluates operators in an expression**.

A simple way to remember the basic order is:

```text
PEMDAS
```

which stands for:

```text
P → Parentheses
E → Exponents
M → Multiplication
D → Division
A → Addition
S → Subtraction
```

Your refresher gives the order as:

1. Parentheses `()`
2. Exponentiation `**`
3. Multiplication `*`, Division `/`, Floor Division `//`, Modulus `%`
4. Addition `+`, Subtraction `-`

---

# 1. Parentheses `()`

Parentheses have the highest priority in the refresher’s basic precedence order.

Example:

```python
result = (10 + 2) * 3

print(result)
```

Output:

```text
36
```

Why?

```text
(10 + 2) * 3
= 12 * 3
= 36
```

Python evaluates the expression inside parentheses first.

---

# 2. Exponentiation `**`

Exponentiation is evaluated before multiplication, division, addition, and subtraction.

Example:

```python
result = 2 ** 3

print(result)
```

Output:

```text
8
```

---

## Important: Exponentiation is Right-to-Left

Example from the refresher:

```python
result = 2 ** 3 ** 2
```

Python evaluates it as:

```text
2 ** (3 ** 2)
```

First:

```text
3 ** 2 = 9
```

Then:

```text
2 ** 9 = 512
```

So:

```python
print(result)
```

Output:

```text
512
```

---

# 3. Multiplication, Division, Floor Division and Modulus

These operators have the same basic precedence level:

```text
*
/
//
%
```

They are evaluated before addition and subtraction.

Example:

```python
result = 10 + 2 * 3
```

Python first evaluates:

```text
2 * 3 = 6
```

Then:

```text
10 + 6 = 16
```

Output:

```text
16
```

This is the same example used in the refresher.

---

# 4. Addition and Subtraction

Addition and subtraction are evaluated after multiplication and division.

Example:

```python
result = 20 - 5 + 2
```

These operations are evaluated from left to right:

```text
20 - 5 = 15
15 + 2 = 17
```

Output:

```text
17
```

---

# Same Precedence → Left to Right

For operators at the same precedence level, the refresher notes that multiplication/division-related operations and addition/subtraction are evaluated from left to right.

Example:

```python
result = 20 / 5 * 2
```

First:

```text
20 / 5 = 4
```

Then:

```text
4 * 2 = 8
```

Output:

```text
8.0
```

---

# Why Parentheses are Useful

Even if you know operator precedence, parentheses make expressions easier to understand.

Without parentheses:

```python
result = 10 + 2 * 3
```

Output:

```text
16
```

With parentheses:

```python
result = (10 + 2) * 3
```

Output:

```text
36
```

Parentheses can completely change the result.

---

# Quick Comparison

### Expression 1

```python
10 + 2 * 3
```

Evaluation:

```text
10 + 6
= 16
```

### Expression 2

```python
(10 + 2) * 3
```

Evaluation:

```text
12 * 3
= 36
```

---

# Basic Precedence Order

```text
Highest
   ↓
()
   ↓
**
   ↓
*  /  //  %
   ↓
+  -
   ↓
Lowest
```

---

# Example

```python
result = 5 + 2 * 3 ** 2
```

Step 1: Exponent

```text
3 ** 2 = 9
```

Step 2: Multiplication

```text
2 * 9 = 18
```

Step 3: Addition

```text
5 + 18 = 23
```

Final output:

```text
23
```

---

# Key Takeaway

Python does not simply evaluate expressions from left to right.

It follows an order of precedence:

```text
Parentheses
    ↓
Exponentiation
    ↓
Multiplication / Division / Floor Division / Modulus
    ↓
Addition / Subtraction
```

When in doubt, use **parentheses** to make the intended order clear.
