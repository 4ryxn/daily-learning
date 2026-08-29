# Tuples and Tuple Methods in Python

A **tuple** in Python is an **ordered and immutable collection of elements**.

It is similar to a list, but once a tuple is created, its elements **cannot be modified**.

---

# Creating a Tuple

Tuples are created using parentheses:

```python
()
```

## Empty Tuple

```python
empty_tuple = ()
```

## Tuple with Elements

```python
numbers = (1, 2, 3, 4, 5)
```

## Mixed Data Types

A tuple can contain values of different data types.

```python
mixed_tuple = (1, "Hello", 3.14, True)
```

These examples are directly shown in the refresher.

---

# Single-Element Tuple

A single-element tuple must contain a **comma**.

Correct:

```python
single_element = (42,)
```

Without the comma:

```python
single_element = (42)
```

Python does not treat it as a tuple.

The refresher specifically notes that the comma is necessary for a single-element tuple.

---

# Important Properties of Tuples

```text
Tuple
  ↓
Ordered
  ↓
Immutable
  ↓
Can contain different data types
```

## Ordered

Tuple elements maintain their position.

```python
fruits = ("apple", "banana", "cherry")
```

The elements have a fixed order.

---

## Immutable

Once a tuple is created, we cannot modify its elements.

For example:

```python
numbers = (1, 2, 3)

numbers[0] = 10
```

This would produce an error because tuples are immutable.

This is the key difference highlighted by the refresher between lists and tuples.

---

# Tuple Indexing

Like lists and strings, tuple indexing starts from `0`.

```python
fruits = ("apple", "banana", "cherry")
```

Indexes:

```text
apple   banana   cherry
  0       1        2
 -3      -2       -1
```

Access first element:

```python
print(fruits[0])
```

Output:

```text
apple
```

Access last element:

```python
print(fruits[-1])
```

Output:

```text
cherry
```

---

# Tuple Slicing

We can also extract part of a tuple using slicing.

```python
numbers = (10, 20, 30, 40, 50)

print(numbers[1:4])
```

Output:

```text
(20, 30, 40)
```

The basic slicing syntax is:

```python
tuple[start:end]
```

---

# Tuple Methods

Because tuples are immutable, they have fewer methods than lists.

The refresher covers two main tuple methods:

```text
count()
index()
```

---

# 1. `count()`

`count()` returns the number of times a value appears in the tuple.

Example:

```python
numbers = (1, 2, 2, 3, 2, 4)

print(numbers.count(2))
```

Output:

```text
3
```

Syntax:

```python
tuple.count(value)
```

The refresher defines `count(x)` as returning the number of times `x` appears in the tuple.

---

# 2. `index()`

`index()` returns the index of the first occurrence of a value.

Example:

```python
numbers = (10, 20, 30, 40)

print(numbers.index(30))
```

Output:

```text
2
```

Syntax:

```python
tuple.index(value)
```

The refresher lists `index(x)` as the second common tuple method.

---

# Tuple vs List

The biggest difference is **mutability**.

| List                      | Tuple                      |
| ------------------------- | -------------------------- |
| Uses `[]`                 | Uses `()`                  |
| Mutable                   | Immutable                  |
| Elements can be changed   | Elements cannot be changed |
| Many modification methods | Only a few methods         |
| Example: `[1, 2, 3]`      | Example: `(1, 2, 3)`       |

The refresher itself defines lists as ordered and mutable, while tuples are ordered and immutable.

---

# Example

## List

```python
numbers = [1, 2, 3]

numbers[0] = 100

print(numbers)
```

Output:

```text
[100, 2, 3]
```

The value can be changed.

---

## Tuple

```python
numbers = (1, 2, 3)

numbers[0] = 100
```

This results in an error because tuple values cannot be modified.

---

# Looping Through a Tuple

Since a tuple is iterable, we can use a `for` loop with it.

```python
fruits = ("apple", "banana", "cherry")

for fruit in fruits:
    print(fruit)
```

Output:

```text
apple
banana
cherry
```

---

# Checking Membership

We can use the `in` operator with tuples.

```python
numbers = (10, 20, 30)

print(20 in numbers)
```

Output:

```text
True
```

---

# When to Use Tuples?

According to the refresher, tuples are useful:

* When you want an **unchangeable collection of elements**
* When you need a **faster alternative to lists**
* When storing **heterogeneous data**, such as database records or coordinates

Example:

```python
coordinates = (28.61, 77.20)
```

A coordinate pair is suitable for a tuple when the values are intended to remain fixed.

---

# Quick Revision

## Create Tuple

```python
numbers = (1, 2, 3)
```

## Empty Tuple

```python
empty_tuple = ()
```

## Single-Element Tuple

```python
single = (10,)
```

## Access Element

```python
numbers[0]
```

## Count Value

```python
numbers.count(2)
```

## Find Index

```python
numbers.index(3)
```

---

# Simple Flow

```text
Tuple
  |
  ├── Ordered
  |
  ├── Immutable
  |
  ├── Supports Indexing
  |
  ├── Supports Slicing
  |
  └── Methods
       ├── count()
       └── index()
```

---

# Key Takeaways

* A tuple is an **ordered and immutable** collection.
* Tuples are similar to lists, but their elements cannot be modified.
* Tuples use `()` instead of `[]`.
* A single-element tuple requires a trailing comma.
* `count()` counts occurrences of a value.
* `index()` returns the first index of a value.
* Tuples are useful when data should remain unchanged.
