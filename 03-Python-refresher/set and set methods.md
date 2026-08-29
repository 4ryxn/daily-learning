# Set and Set Methods in Python

A **set** in Python is an **unordered, mutable collection of unique elements**.

A set does **not allow duplicate values**.

---

# Creating a Set

Sets are generally created using curly braces:

```python id="amk1pt"
{}
```

But an **empty set must be created using `set()`**, because `{}` creates an empty dictionary instead.

## Empty Set

```python id="q8h7df"
empty_set = set()
```

## Set with Elements

```python id="v2pw9h"
numbers = {1, 2, 3, 4, 5}
```

## Mixed Data Types

```python id="t6hs91"
mixed_set = {1, "Hello", 3.14, True}
```

These forms are shown in the refresher.

---

# Sets Do Not Allow Duplicates

If duplicate values are provided, Python keeps only the unique values.

Example from the refresher:

```python id="29nzp3"
unique_numbers = set([1, 2, 2, 3, 4, 4, 5])

print(unique_numbers)
```

Output:

```text id="m02t81"
{1, 2, 3, 4, 5}
```

This makes sets useful when we want to remove duplicate values.

---

# Important Properties of Sets

```text id="vbhk6m"
Set
 ↓
Unordered
 ↓
Mutable
 ↓
Unique Elements
 ↓
No Duplicates
```

## Unordered

Sets do not maintain a fixed positional order like lists or tuples.

Therefore, we normally do not access elements using indexes.

---

## Mutable

A set can be modified after creation.

We can:

* Add elements
* Remove elements
* Add multiple elements
* Clear all elements

---

# Common Set Methods

The refresher covers:

```text id="5n88er"
add()
update()
remove()
discard()
pop()
clear()
copy()
```

---

# 1. `add()`

`add()` adds one element to a set.

Example:

```python id="f91n8h"
numbers = {1, 2, 3}

numbers.add(4)

print(numbers)
```

Output may contain:

```text id="48qqgk"
{1, 2, 3, 4}
```

Syntax:

```python id="8jyyv5"
set.add(value)
```

The refresher defines `add(x)` as adding an element `x` to the set.

---

# 2. `update()`

`update()` adds multiple elements from another iterable.

Example:

```python id="tz88cq"
numbers = {1, 2, 3}

numbers.update([4, 5, 6])

print(numbers)
```

The set now contains:

```text id="hw3do3"
{1, 2, 3, 4, 5, 6}
```

Syntax:

```python id="qjz3df"
set.update(iterable)
```

The refresher uses:

```python id="ro3lmt"
my_set.update([6, 7, 8])
```

---

# `add()` vs `update()`

```text id="su93tf"
add()
 ↓
Adds one element
```

```text id="fw0dbt"
update()
 ↓
Adds multiple elements
```

Example:

```python id="an315h"
numbers.add(4)
```

vs.

```python id="njkz8a"
numbers.update([4, 5, 6])
```

---

# 3. `remove()`

`remove()` removes a particular value from the set.

```python id="7yk220"
numbers = {1, 2, 3, 4}

numbers.remove(3)

print(numbers)
```

The value `3` is removed.

Important:

If the value is not found, `remove()` raises an error.

The refresher specifically states this behavior.

---

# 4. `discard()`

`discard()` also removes an element.

```python id="bsoqfp"
numbers = {1, 2, 3}

numbers.discard(2)
```

The important difference is that `discard()` **does not raise an error if the value does not exist**.

---

# `remove()` vs `discard()`

This is an important difference.

```text id="qaf16v"
remove(x)
   ↓
Value missing?
   ↓
Error
```

```text id="sddtr3"
discard(x)
   ↓
Value missing?
   ↓
No error
```

Example:

```python id="icqpsd"
numbers = {1, 2, 3}

numbers.remove(10)
```

This raises an error.

But:

```python id="bimr76"
numbers.discard(10)
```

does not.

---

# 5. `pop()`

`pop()` removes and returns an element from the set.

```python id="vn7c71"
numbers = {1, 2, 3}

removed = numbers.pop()

print(removed)
```

Since sets are unordered, you should not rely on `pop()` removing a specific position.

The refresher describes `pop()` as removing and returning a random element.

---

# 6. `clear()`

`clear()` removes every element from the set.

```python id="a2d8jq"
numbers = {1, 2, 3}

numbers.clear()

print(numbers)
```

Output:

```text id="2wzyia"
set()
```

The set still exists but becomes empty.

---

# 7. `copy()`

`copy()` creates a shallow copy of a set.

```python id="cs5brp"
numbers = {1, 2, 3}

new_set = numbers.copy()

print(new_set)
```

The refresher uses:

```python id="80jzmh"
new_set = my_set.copy()
```

---

# Set Operations

Sets are especially useful because we can perform mathematical set operations such as:

```text id="937sp8"
Union
Intersection
Difference
Symmetric Difference
Subset
Superset
```

---

# 1. Union

A union combines all unique elements from both sets.

Example:

```python id="pzufws"
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

print(set1.union(set2))
```

Result:

```text id="5z0r90"
{1, 2, 3, 4, 5, 6}
```

The refresher defines `union()` as returning a new set containing all unique elements from both sets.

---

# Union Operator `|`

Python also provides the `|` operator.

```python id="90fw5p"
print(set1 | set2)
```

Output:

```text id="q8kgof"
{1, 2, 3, 4, 5, 6}
```

The refresher shows both versions:

```python id="v42q5e"
set1 | set2
set1.union(set2)
```

as equivalent ways to perform union.

---

# 2. Intersection

Intersection returns values that are present in **both sets**.

```python id="u5fbqq"
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

print(set1.intersection(set2))
```

Result:

```text id="nqty2n"
{3, 4}
```

---

# Intersection Operator `&`

The same operation can be written using:

```python id="k4oxvx"
print(set1 & set2)
```

The refresher uses this operator example and gets `{3, 4}`.

---

# 3. Difference

Difference returns values that are present in the first set but **not present in the second set**.

```python id="nndyxi"
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

print(set1.difference(set2))
```

Result:

```text id="60ox9u"
{1, 2}
```

The refresher defines it as elements in `set1` but not in `set2`.

---

# Difference Operator `-`

Difference can also be written as:

```python id="mwnu19"
set1 - set2
```

---

# 4. Symmetric Difference

Symmetric difference returns elements that appear in **either set, but not both**.

Example:

```python id="dfj9wr"
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

print(set1.symmetric_difference(set2))
```

Result:

```text id="f6ezun"
{1, 2, 5, 6}
```

Common values `3` and `4` are not included.

---

# Symmetric Difference Operator `^`

The refresher notes that symmetric difference can also be performed using:

```python id="in141k"
set1 ^ set2
```

It lists the following operator equivalents:

```text id="1nlslk"
Union               → |
Intersection        → &
Difference          → -
Symmetric Difference → ^
```

---

# 5. `issubset()`

`issubset()` checks whether every element of one set exists inside another set.

Example:

```python id="o5fg40"
set1 = {1, 2}
set2 = {1, 2, 3, 4}

print(set1.issubset(set2))
```

Output:

```text id="ut6jon"
True
```

The refresher defines `issubset(set2)` as returning `True` when `set1` is a subset of `set2`.

---

# 6. `issuperset()`

`issuperset()` checks whether one set contains all elements of another set.

```python id="u22ka8"
set1 = {1, 2, 3, 4}
set2 = {1, 2}

print(set1.issuperset(set2))
```

Output:

```text id="fby7n8"
True
```

The refresher defines it as returning `True` when `set1` is a superset of `set2`.

---

# Set Operations Summary

| Operation            | Method                   | Operator | Purpose                                   |
| -------------------- | ------------------------ | -------- | ----------------------------------------- |
| Union                | `union()`                | `\|`     | All unique elements                       |
| Intersection         | `intersection()`         | `&`      | Common elements                           |
| Difference           | `difference()`           | `-`      | Elements only in first set                |
| Symmetric Difference | `symmetric_difference()` | `^`      | Elements in either set, but not both      |
| Subset               | `issubset()`             | —        | Check whether set is contained in another |
| Superset             | `issuperset()`           | —        | Check whether set contains another        |

---

# Common Set Methods Summary

| Method                   | Purpose                                       |
| ------------------------ | --------------------------------------------- |
| `add(x)`                 | Add one element                               |
| `update(iterable)`       | Add multiple elements                         |
| `remove(x)`              | Remove element; error if missing              |
| `discard(x)`             | Remove element; no error if missing           |
| `pop()`                  | Remove and return an element                  |
| `clear()`                | Remove all elements                           |
| `copy()`                 | Create a shallow copy                         |
| `union()`                | Combine unique elements                       |
| `intersection()`         | Find common elements                          |
| `difference()`           | Find elements only in first set               |
| `symmetric_difference()` | Find elements present in either, but not both |
| `issubset()`             | Check subset                                  |
| `issuperset()`           | Check superset                                |

---

# Quick Revision

## Create Set

```python id="sxa592"
numbers = {1, 2, 3}
```

## Empty Set

```python id="1b1uq1"
numbers = set()
```

## Add One Element

```python id="9tkezf"
numbers.add(4)
```

## Add Multiple Elements

```python id="tcsliy"
numbers.update([4, 5, 6])
```

## Remove

```python id="qomby8"
numbers.remove(2)
```

## Remove Safely

```python id="lavvks"
numbers.discard(2)
```

## Union

```python id="0frsdm"
set1 | set2
```

## Intersection

```python id="lmq3v6"
set1 & set2
```

## Difference

```python id="fybp29"
set1 - set2
```

## Symmetric Difference

```python id="mtygqq"
set1 ^ set2
```

---

# Simple Flow

```text id="38o94c"
Set
 |
 ├── Add
 |    ├── add()
 |    └── update()
 |
 ├── Remove
 |    ├── remove()
 |    ├── discard()
 |    ├── pop()
 |    └── clear()
 |
 ├── Copy
 |    └── copy()
 |
 └── Operations
      ├── union()
      ├── intersection()
      ├── difference()
      ├── symmetric_difference()
      ├── issubset()
      └── issuperset()
```

---

# Key Takeaways

* Sets are **unordered, mutable, and contain unique values**.
* Duplicate values are automatically removed.
* Use `set()` to create an empty set.
* `add()` adds one element.
* `update()` adds multiple elements.
* `remove()` raises an error if an element is missing.
* `discard()` does not raise an error if an element is missing.
* Sets support union, intersection, difference, and symmetric difference.
* These operations can be performed using both methods and operators.
