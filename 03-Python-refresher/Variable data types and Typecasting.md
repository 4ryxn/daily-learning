# Variables, Data Types and Typecasting in Python

## What is a Variable?

A variable is a **container used to store a value**.

Example:

```python
name = "Alice"
age = 25
is_student = True
```

Here:

* `name` stores a string
* `age` stores an integer
* `is_student` stores a Boolean value

Python does not require us to explicitly declare the data type of a variable.

---

# Data Types in Python

A data type tells Python what kind of value is stored inside a variable.

## Common Data Types

| Data Type | Example         | Description                   |
| --------- | --------------- | ----------------------------- |
| `int`     | `10`, `-5`      | Integer numbers               |
| `float`   | `3.14`, `-0.5`  | Decimal numbers               |
| `str`     | `"hello"`       | Text                          |
| `bool`    | `True`, `False` | Boolean values                |
| `list`    | `[1, 2, 3]`     | Ordered, mutable collection   |
| `tuple`   | `(1, 2, 3)`     | Ordered, immutable collection |
| `dict`    | `{"a": 1}`      | Key-value pairs               |

---

# 1. Integer — `int`

Integers are whole numbers.

```python
age = 21
temperature = -5
```

Examples:

```text
10
0
-25
500
```

---

# 2. Float — `float`

Floats contain decimal values.

```python
price = 99.99
height = 5.7
```

Examples:

```text
3.14
-0.5
10.0
```

---

# 3. String — `str`

Strings store text.

```python
name = "Aryan"
language = "Python"
```

---

# 4. Boolean — `bool`

Boolean values represent:

```text
True
False
```

Example:

```python
is_student = True
is_logged_in = False
```

---

# 5. List — `list`

A list stores multiple values.

```python
numbers = [1, 2, 3, 4]
```

Lists are **mutable**, which means their contents can be changed.

Example:

```python
numbers[0] = 100
```

---

# 6. Tuple — `tuple`

A tuple also stores multiple values.

```python
coordinates = (10, 20)
```

Tuples are **immutable**, which means their contents cannot be changed after creation.

---

# 7. Dictionary — `dict`

A dictionary stores data using **key-value pairs**.

```python
student = {
    "name": "Alice",
    "age": 25
}
```

Here:

```text
"name" → Key
"Alice" → Value
```

---

# Checking the Data Type

Python provides the `type()` function.

Example:

```python
age = 25

print(type(age))
```

Output:

```text
<class 'int'>
```

Another example:

```python
name = "Python"

print(type(name))
```

Output:

```text
<class 'str'>
```

---

# What is Typecasting?

Typecasting means **converting a value from one data type to another**.

Python provides built-in functions such as:

```text
int()
float()
str()
list()
```

---

## String to Integer

```python
x = int("10")

print(x)
```

Output:

```text
10
```

Now `x` is an integer.

---

## Integer to String

```python
age = 25

text_age = str(age)
```

Now:

```python
type(text_age)
```

returns:

```text
str
```

---

## Float to Integer

```python
x = int(3.9)

print(x)
```

Output:

```text
3
```

Important:

`int()` **truncates the decimal part**.

It does not round the number.

---

## String to List

```python
letters = list("abc")

print(letters)
```

Output:

```python
['a', 'b', 'c']
```

---

# Typecasting Errors

Not every value can be converted into every data type.

Example:

```python
x = int("hello")
```

This causes:

```text
ValueError
```

because `"hello"` cannot be converted into an integer.

---

# Simple Example

```python
age = "21"

print(type(age))

age = int(age)

print(type(age))
```

Before conversion:

```text
str
```

After conversion:

```text
int
```

---

# Quick Revision

```text
int()   → Convert to integer
float() → Convert to decimal number
str()   → Convert to string
list()  → Convert to list
```

---

## Key Takeaway

Variables store values, while data types define what kind of values they contain.

Typecasting allows us to convert values from one compatible data type to another.
