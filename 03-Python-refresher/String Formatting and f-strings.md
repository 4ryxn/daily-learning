# String Formatting and f-Strings in Python

String formatting means **inserting values inside a string in a clean and readable way**.

Your Python Refresher explains two main approaches:

1. `format()`
2. **f-strings** — the recommended modern approach

It also notes that f-strings were introduced in **Python 3.6**.

---

# 1. Using `format()`

The `format()` method inserts values inside `{}` placeholders.

## Basic Example

```python
name = "Alice"
age = 25

print("My name is {} and I am {} years old.".format(name, age))
```

Output:

```text
My name is Alice and I am 25 years old.
```

---

# Positional Arguments

We can control where values appear using indexes.

```python
print("{0} is learning {1}".format("Alice", "Python"))
```

Output:

```text
Alice is learning Python
```

Here:

```text
{0} → Alice
{1} → Python
```

---

# Keyword Arguments

We can also give names to placeholders.

```python
print(
    "{name} is learning {language}".format(
        name="Alice",
        language="Python"
    )
)
```

Output:

```text
Alice is learning Python
```

The refresher covers both positional and keyword arguments with `format()`.

---

# 2. f-Strings

f-strings provide a **cleaner and more readable** way to format strings.

Syntax:

```python
f"Text {variable}"
```

The letter `f` is written before the opening quote.

---

# Basic f-String Example

```python
name = "Alice"
age = 25

print(f"My name is {name} and I am {age} years old.")
```

Output:

```text
My name is Alice and I am 25 years old.
```

Instead of writing:

```python
"My name is {} and I am {} years old.".format(name, age)
```

we can directly put variables inside `{}`.

---

# Expressions Inside f-Strings

f-strings can contain expressions.

Example from the refresher:

```python
a = 5
b = 10

print(f"Sum of {a} and {b} is {a + b}")
```

Output:

```text
Sum of 5 and 10 is 15
```

Python evaluates:

```text
{a + b}
```

before inserting the result into the string.

---

# Formatting Numbers

f-strings can also control how numbers are displayed.

Example:

```python
pi = 3.14159

print(f"Pi rounded to 2 decimal places: {pi:.2f}")
```

Output:

```text
Pi rounded to 2 decimal places: 3.14
```

Here:

```text
.2f
```

means:

```text
Display the floating-point number
with 2 digits after the decimal
```

This example appears directly in the refresher.

---

# Padding and Alignment

The refresher also shows formatting text width and alignment.

## Left Align

```python
print(f"{'Python':<10}")
```

`<` means:

```text
Left align
```

inside a width of `10` characters.

---

## Right Align

```python
print(f"{'Python':>10}")
```

`>` means:

```text
Right align
```

---

## Center Align

```python
print(f"{'Python':^10}")
```

`^` means:

```text
Center align
```

The refresher demonstrates all three alignment options.

---

# Quick Alignment Summary

| Symbol | Meaning      |
| ------ | ------------ |
| `<`    | Left align   |
| `>`    | Right align  |
| `^`    | Center align |

Example:

```python
word = "Python"

print(f"{word:<10}")
print(f"{word:>10}")
print(f"{word:^10}")
```

---

# `format()` vs f-Strings

## Using `format()`

```python
name = "Alice"
age = 25

print("My name is {} and I am {} years old.".format(name, age))
```

## Using f-String

```python
name = "Alice"
age = 25

print(f"My name is {name} and I am {age} years old.")
```

The f-string version is shorter and easier to read.

Your refresher recommends f-strings as the preferred modern formatting approach.

---

# Quick Examples

## Insert a Variable

```python
language = "Python"

print(f"I am learning {language}")
```

Output:

```text
I am learning Python
```

---

## Insert Multiple Variables

```python
name = "Alice"
score = 90

print(f"{name} scored {score} marks.")
```

Output:

```text
Alice scored 90 marks.
```

---

## Perform Calculation

```python
price = 100
quantity = 3

print(f"Total price = {price * quantity}")
```

Output:

```text
Total price = 300
```

---

## Format Decimal Value

```python
value = 12.34567

print(f"{value:.2f}")
```

Output:

```text
12.35
```

---

# Basic Flow

```text
Variables / Expressions
        ↓
       { }
        ↓
     f-string
        ↓
Formatted Output
```

Example:

```python
name = "Alice"

print(f"Hello {name}")
```

---

# Quick Revision

## `format()`

```python
"Hello {}".format(name)
```

## f-String

```python
f"Hello {name}"
```

## Expression

```python
f"{a + b}"
```

## Two Decimal Places

```python
f"{value:.2f}"
```

## Left Alignment

```python
f"{text:<10}"
```

## Right Alignment

```python
f"{text:>10}"
```

## Center Alignment

```python
f"{text:^10}"
```

---

# Key Takeaways

* String formatting helps insert values into text.
* `format()` uses `{}` placeholders.
* `format()` supports positional and keyword arguments.
* f-strings use the syntax `f"..."`.
* Variables and expressions can be written directly inside `{}`.
* f-strings can format decimal values.
* `<`, `>`, and `^` can be used for alignment.
* The refresher recommends **f-strings** because they are cleaner and more readable.
