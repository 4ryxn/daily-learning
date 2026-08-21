# Taking Input from the User in Python

Python allows us to take input from the user using the built-in:

```python
input()
```

function.

The uploaded refresher notes emphasize one important rule:

> `input()` always returns a string.

---

# Basic Syntax

```python
variable = input("Message for user: ")
```

Example:

```python
name = input("Enter your name: ")

print("Hello", name)
```

If the user enters:

```text
Aryan
```

Output:

```text
Hello Aryan
```

---

# Important: `input()` Returns a String

Even if the user enters a number, Python initially treats it as a string.

Example:

```python
age = input("Enter your age: ")

print(type(age))
```

If the user enters:

```text
21
```

the data type will still be:

```text
<class 'str'>
```

This is why type conversion is often required when taking numerical input.

---

# Taking Integer Input

We can convert the input to an integer using:

```python
int()
```

Example:

```python
age = int(input("Enter your age: "))

print(age)
print(type(age))
```

Now the type becomes:

```text
<class 'int'>
```

The refresher specifically shows converting user input using `int()` for values such as age.

---

# Taking Float Input

For decimal numbers, use:

```python
float()
```

Example:

```python
price = float(input("Enter the price: "))

print(price)
print(type(price))
```

If the user enters:

```text
99.50
```

Python stores it as a floating-point value.

The refresher also demonstrates this pattern for price input.

---

# Example: Add Two Numbers

Without typecasting:

```python
a = input("Enter first number: ")
b = input("Enter second number: ")

print(a + b)
```

If the user enters:

```text
10
20
```

the result will be:

```text
1020
```

because both values are strings.

---

## Correct Way

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))

print(a + b)
```

Output:

```text
30
```

---

# String Input

If you want text input, no conversion is needed.

Example:

```python
city = input("Enter your city: ")

print("City:", city)
```

---

# Integer Input

```python
age = int(input("Enter your age: "))
```

---

# Float Input

```python
price = float(input("Enter the price: "))
```

---

# Multiple Inputs

We can take multiple inputs separately.

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
city = input("Enter your city: ")

print(name, age, city)
```

---

# Using Input with f-Strings

```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))

print(f"My name is {name} and I am {age} years old.")
```

Example output:

```text
My name is Aryan and I am 21 years old.
```

---

# Simple Calculator Example

```python
a = float(input("Enter first number: "))
b = float(input("Enter second number: "))

sum_result = a + b

print("Sum:", sum_result)
```

---

# Type Conversion Flow

```text
User enters value
       ↓
input()
       ↓
Value is stored as str
       ↓
Need a number?
       ↓
int() or float()
       ↓
Use value in calculations
```

---

# Common Mistake

```python
age = input("Enter age: ")

print(age + 5)
```

This causes an error because `age` is a string while `5` is an integer.

Correct version:

```python
age = int(input("Enter age: "))

print(age + 5)
```

---

# Quick Revision

| Requirement   | Code             |
| ------------- | ---------------- |
| Text input    | `input()`        |
| Integer input | `int(input())`   |
| Decimal input | `float(input())` |

Example:

```python
name = input("Enter name: ")
age = int(input("Enter age: "))
price = float(input("Enter price: "))
```

---

## Key Takeaway

The main rule to remember is:

```text
input() → always returns a string
```

If numerical data is required, convert it explicitly:

```python
int(input())
```

or:

```python
float(input())
```
