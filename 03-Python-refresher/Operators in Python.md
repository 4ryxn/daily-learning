# Operators in Python

Operators are symbols or keywords used to perform operations on values and variables.

Example:

```python
a = 10
b = 5

result = a + b
```

Here:

```text
+
```

is an operator.

---

# Types of Operators

Python provides several types of operators:

1. Arithmetic Operators
2. Comparison Operators
3. Logical Operators
4. Bitwise Operators
5. Assignment Operators
6. Membership Operators
7. Identity Operators

---

# 1. Arithmetic Operators

Arithmetic operators perform mathematical operations.

Assume:

```python
a = 10
b = 5
```

| Operator | Meaning        | Example  | Result   |
| -------- | -------------- | -------- | -------- |
| `+`      | Addition       | `a + b`  | `15`     |
| `-`      | Subtraction    | `a - b`  | `5`      |
| `*`      | Multiplication | `a * b`  | `50`     |
| `/`      | Division       | `a / b`  | `2.0`    |
| `//`     | Floor Division | `a // b` | `2`      |
| `%`      | Modulus        | `a % b`  | `0`      |
| `**`     | Exponentiation | `a ** b` | `100000` |

---

## Division `/`

Normal division produces a floating-point value.

```python
10 / 5
```

Output:

```text
2.0
```

---

## Floor Division `//`

Floor division returns the floor value of division.

```python
10 // 3
```

Output:

```text
3
```

---

## Modulus `%`

Returns the remainder.

```python
10 % 3
```

Output:

```text
1
```

Useful for tasks such as checking even and odd numbers.

```python
number = 10

number % 2
```

If the result is `0`, the number is even.

---

## Exponentiation `**`

Used for powers.

```python
2 ** 3
```

Output:

```text
8
```

---

# 2. Comparison Operators

Comparison operators compare two values.

Their result is:

```text
True
```

or:

```text
False
```

Assume:

```python
a = 10
b = 5
```

| Operator | Meaning               | Result  |
| -------- | --------------------- | ------- |
| `==`     | Equal                 | `False` |
| `!=`     | Not equal             | `True`  |
| `>`      | Greater than          | `True`  |
| `<`      | Less than             | `False` |
| `>=`     | Greater than or equal | `True`  |
| `<=`     | Less than or equal    | `False` |

Example:

```python
age = 20

print(age >= 18)
```

Output:

```text
True
```

---

# 3. Logical Operators

Logical operators combine multiple conditions.

Python has:

```text
and
or
not
```

---

## `and`

Returns `True` when both conditions are true.

```python
age = 25

age >= 18 and age <= 60
```

Output:

```text
True
```

---

## `or`

Returns `True` when at least one condition is true.

```python
day = "Sunday"

day == "Saturday" or day == "Sunday"
```

Output:

```text
True
```

---

## `not`

Reverses a Boolean value.

```python
x = True

not x
```

Output:

```text
False
```

---

# 4. Bitwise Operators

Bitwise operators perform operations on the binary representation of integers.

Assume:

```python
a = 5
b = 3
```

Binary:

```text
5 = 101
3 = 011
```

## Bitwise AND `&`

```python
5 & 3
```

Output:

```text
1
```

---

## Bitwise OR `|`

```python
5 | 3
```

Output:

```text
7
```

---

# 5. Assignment Operators

Assignment operators are used to assign or update values.

```python
a = 10
```

## Basic Assignment

```python
a = 5
```

---

## Addition Assignment

```python
a += 5
```

Equivalent to:

```python
a = a + 5
```

---

## Common Assignment Operators

| Operator | Example   | Equivalent   |
| -------- | --------- | ------------ |
| `=`      | `a = 5`   | `a = 5`      |
| `+=`     | `a += 5`  | `a = a + 5`  |
| `-=`     | `a -= 5`  | `a = a - 5`  |
| `*=`     | `a *= 5`  | `a = a * 5`  |
| `/=`     | `a /= 5`  | `a = a / 5`  |
| `//=`    | `a //= 5` | `a = a // 5` |
| `%=`     | `a %= 5`  | `a = a % 5`  |
| `**=`    | `a **= 5` | `a = a ** 5` |

---

# 6. Membership Operators

Membership operators check whether a value exists inside a sequence.

Python provides:

```text
in
not in
```

Example:

```python
numbers = [1, 2, 3]

2 in numbers
```

Output:

```text
True
```

---

## `not in`

```python
5 not in numbers
```

Output:

```text
True
```

Membership operators can also be used with strings.

```python
"Py" in "Python"
```

Output:

```text
True
```

---

# 7. Identity Operators

Identity operators check whether two variables refer to the **same object**.

Python provides:

```text
is
is not
```

Example:

```python
a is b
```

or:

```python
a is not b
```

Important:

```text
== → compares values

is → compares object identity
```

These are not the same operation.

---

# Operator Precedence

When multiple operators occur in one expression, Python follows an order of evaluation.

A useful basic rule is:

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

---

## Example

```python
result = 10 + 2 * 3

print(result)
```

Output:

```text
16
```

Multiplication happens first:

```text
10 + (2 × 3)
10 + 6
16
```

---

## Parentheses First

```python
result = (10 + 2) * 3
```

Output:

```text
36
```

Because:

```text
(10 + 2) × 3
12 × 3
36
```

---

# Exponentiation

Exponentiation is evaluated right-to-left.

Example:

```python
2 ** 3 ** 2
```

is evaluated as:

```text
2 ** (3 ** 2)
```

Therefore:

```text
2 ** 9
= 512
```

---

# Quick Revision

```text
Arithmetic  → + - * / // % **
Comparison  → == != > < >= <=
Logical     → and or not
Bitwise     → & |
Assignment  → = += -= *= /= ...
Membership  → in, not in
Identity    → is, is not
```

## Key Takeaway

Operators allow Python programs to perform:

* Calculations
* Comparisons
* Logical decisions
* Variable updates
* Membership checks
* Object identity checks

Understanding operators is essential because they are used throughout Python programs, especially inside conditions, loops, and Data Science logic.
