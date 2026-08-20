# Strings and String Methods in Python

## What is a String?

A string is a **sequence of characters** enclosed inside single or double quotes.

Example:

```python
name = "Alice"
language = 'Python'
```

Both are valid strings.

---

# Multiline Strings

For text containing multiple lines, Python allows triple quotes.

Example:

```python
message = """This is
a multiline
string."""
```

Triple single quotes can also be used:

```python
message = '''Hello
Python
World'''
```

---

# String Indexing

Each character in a string has an index.

Python indexing starts from:

```text
0
```

Example:

```python
text = "Python"
```

Indexes:

```text
 P   y   t   h   o   n
 0   1   2   3   4   5
-6  -5  -4  -3  -2  -1
```

Access first character:

```python
text[0]
```

Output:

```text
'P'
```

Access last character:

```python
text[-1]
```

Output:

```text
'n'
```

---

# String Slicing

Slicing allows us to extract part of a string.

Syntax:

```python
string[start:end]
```

The `end` index is not included.

Example:

```python
text = "Python"

print(text[0:2])
```

Output:

```text
Py
```

---

## More Examples

```python
text[:3]
```

Output:

```text
Pyt
```

```python
text[3:]
```

Output:

```text
hon
```

---

# String Immutability

Strings are **immutable**.

This means individual characters cannot be modified after the string is created.

Example:

```python
text = "Python"

text[0] = "J"
```

This produces an error.

Instead, we need to create a new string.

---

# Common String Methods

Python provides many built-in methods for manipulating strings.

## `lower()`

Converts text to lowercase.

```python
"HELLO".lower()
```

Output:

```text
hello
```

---

## `upper()`

Converts text to uppercase.

```python
"hello".upper()
```

Output:

```text
HELLO
```

---

## `strip()`

Removes spaces from the beginning and end of a string.

```python
" Hello ".strip()
```

Output:

```text
Hello
```

---

## `replace()`

Replaces part of a string.

```python
text = "I like Java"

text.replace("Java", "Python")
```

Output:

```text
I like Python
```

---

## `split()`

Splits a string into a list.

```python
"hello world".split()
```

Output:

```python
['hello', 'world']
```

---

## `join()`

Combines multiple strings into one string.

Example:

```python
"-".join(["2025", "04", "14"])
```

Output:

```text
2025-04-14
```

---

## `find()`

Returns the index of the first occurrence of a substring.

```python
"python".find("th")
```

Output:

```text
2
```

---

## `count()`

Counts how many times a substring appears.

```python
"banana".count("a")
```

Output:

```text
3
```

---

## `startswith()`

Checks whether a string starts with a particular value.

```python
"Python".startswith("Py")
```

Output:

```text
True
```

---

## `endswith()`

Checks whether a string ends with a particular value.

```python
"python.py".endswith(".py")
```

Output:

```text
True
```

---

## `isdigit()`

Checks whether every character is a digit.

```python
"12345".isdigit()
```

Output:

```text
True
```

---

## `isalpha()`

Checks whether every character contains letters.

```python
"Python".isalpha()
```

Output:

```text
True
```

---

## `isalnum()`

Checks whether the string contains only letters and numbers.

```python
"Python123".isalnum()
```

Output:

```text
True
```

---

# String Methods Summary

| Method         | Purpose               |
| -------------- | --------------------- |
| `lower()`      | Convert to lowercase  |
| `upper()`      | Convert to uppercase  |
| `strip()`      | Remove outer spaces   |
| `replace()`    | Replace text          |
| `split()`      | String → List         |
| `join()`       | List → String         |
| `find()`       | Find substring index  |
| `count()`      | Count occurrences     |
| `startswith()` | Check beginning       |
| `endswith()`   | Check ending          |
| `isdigit()`    | Check digits          |
| `isalpha()`    | Check letters         |
| `isalnum()`    | Check letters/numbers |

---

# String Formatting with f-Strings

Python supports **f-strings** for inserting values inside strings.

Example:

```python
name = "Alice"
age = 30

message = f"Hello, {name}. You are {age} years old."

print(message)
```

Output:

```text
Hello, Alice. You are 30 years old.
```

---

# Expressions Inside f-Strings

We can also perform calculations.

```python
a = 5
b = 10

print(f"Sum of {a} and {b} is {a + b}")
```

Output:

```text
Sum of 5 and 10 is 15
```

---

# Formatting Numbers

Example:

```python
pi = 3.14159

print(f"{pi:.2f}")
```

Output:

```text
3.14
```

---

# Quick Revision

```text
String
 ↓
Indexing
 ↓
Slicing
 ↓
String Methods
 ↓
Formatting
```

## Key Takeaway

Strings are immutable sequences of characters.

Python provides many built-in string methods that make cleaning, searching, splitting, replacing, and formatting text easy.
