# List and List Methods in Python

A **list** in Python is an **ordered and mutable collection of elements**.

A list can also contain elements of different data types.

---

# Creating a List

Lists are created using square brackets:

```python
[]
```

## Empty List

```python
my_list = []
```

## List with Elements

```python
numbers = [1, 2, 3, 4, 5]
```

## Mixed Data Types

A list can store different types of values together.

```python
mixed_list = [1, "Hello", 3.14, True]
```

## These forms are shown in the refresher.

# Important Properties of Lists

```text
List
 ↓
Ordered
 ↓
Mutable
 ↓
Can contain different data types
```

### Ordered

Elements maintain their position.

```python
fruits = ["apple", "banana", "cherry"]
```

Here:

```text
apple  → first
banana → second
cherry → third
```

### Mutable

Mutable means a list can be modified after creation.

We can:

* Add elements
* Remove elements
* Sort elements
* Reverse elements
* Clear the list

---

# Common List Methods

The refresher covers these major methods:

```text
append()
extend()
insert()
remove()
pop()
index()
count()
sort()
reverse()
copy()
clear()
```

---

# 1. `append()`

`append()` adds one element to the **end of a list**.

```python
fruits = ["apple", "banana"]

fruits.append("orange")

print(fruits)
```

Output:

```text
['apple', 'banana', 'orange']
```

Syntax:

```python
list.append(value)
```

The refresher defines `append(x)` as adding `x` to the end of the list.

---

# 2. `extend()`

`extend()` adds **multiple elements** from another iterable.

```python
numbers = [1, 2, 3]

numbers.extend([4, 5, 6])

print(numbers)
```

Output:

```text
[1, 2, 3, 4, 5, 6]
```

Syntax:

```python
list.extend(iterable)
```

---

# `append()` vs `extend()`

This is an important difference.

## `append()`

```python
numbers = [1, 2]

numbers.append([3, 4])

print(numbers)
```

Output:

```text
[1, 2, [3, 4]]
```

The entire list `[3, 4]` becomes **one element**.

---

## `extend()`

```python
numbers = [1, 2]

numbers.extend([3, 4])

print(numbers)
```

Output:

```text
[1, 2, 3, 4]
```

The elements are added individually.

Quick difference:

```text
append() → Add one item

extend() → Add multiple items
```

---

# 3. `insert()`

`insert()` adds an element at a specified index.

Syntax:

```python
list.insert(index, value)
```

Example:

```python
languages = ["Python", "Java"]

languages.insert(1, "C++")

print(languages)
```

Output:

```text
['Python', 'C++', 'Java']
```

The refresher uses the form `my_list.insert(2, "Python")`.

---

# 4. `remove()`

`remove()` removes the **first occurrence** of a particular value.

```python
numbers = [1, 2, 3, 2]

numbers.remove(2)

print(numbers)
```

Output:

```text
[1, 3, 2]
```

Only the first `2` is removed.

Syntax:

```python
list.remove(value)
```

---

# 5. `pop()`

`pop()` removes and returns an element.

Syntax:

```python
list.pop(index)
```

Example:

```python
numbers = [10, 20, 30]

removed = numbers.pop(1)

print(removed)
print(numbers)
```

Output:

```text
20
[10, 30]
```

If no index is provided, `pop()` removes the last element.

```python
numbers = [10, 20, 30]

numbers.pop()

print(numbers)
```

Output:

```text
[10, 20]
```

The refresher specifies that `pop([index])` removes and returns the indexed element, or the last element when no index is supplied.

---

# `remove()` vs `pop()`

```text
remove(value)
      ↓
Remove using the value
```

```text
pop(index)
      ↓
Remove using the index
and return the removed element
```

Example:

```python
numbers = [10, 20, 30]

numbers.remove(20)
```

vs.

```python
numbers = [10, 20, 30]

numbers.pop(1)
```

Both remove `20`, but they work differently.

---

# 6. `index()`

`index()` returns the index of the **first occurrence** of a value.

Example:

```python
numbers = [10, 20, 30, 20]

print(numbers.index(20))
```

Output:

```text
1
```

Syntax:

```python
list.index(value)
```

---

# 7. `count()`

`count()` tells us how many times a value occurs in a list.

```python
numbers = [1, 2, 2, 3, 2]

print(numbers.count(2))
```

Output:

```text
3
```

Syntax:

```python
list.count(value)
```

---

# 8. `sort()`

`sort()` sorts a list in ascending order.

Example:

```python
numbers = [5, 2, 4, 1, 3]

numbers.sort()

print(numbers)
```

Output:

```text
[1, 2, 3, 4, 5]
```

The refresher defines `sort()` as sorting the list in ascending order.

---

## Sorting Strings

```python
fruits = ["orange", "apple", "banana"]

fruits.sort()

print(fruits)
```

Output:

```text
['apple', 'banana', 'orange']
```

The refresher also shows a fruit list being appended to and then sorted.

---

# 9. `reverse()`

`reverse()` reverses the current order of a list.

```python
numbers = [1, 2, 3, 4]

numbers.reverse()

print(numbers)
```

Output:

```text
[4, 3, 2, 1]
```

Syntax:

```python
list.reverse()
```

---

# 10. `copy()`

`copy()` creates a **shallow copy** of a list.

```python
numbers = [1, 2, 3]

new_list = numbers.copy()

print(new_list)
```

Output:

```text
[1, 2, 3]
```

Syntax:

```python
new_list = old_list.copy()
```

---

# 11. `clear()`

`clear()` removes every element from the list.

```python
numbers = [1, 2, 3]

numbers.clear()

print(numbers)
```

Output:

```text
[]
```

The list still exists, but it becomes empty.

---

# Example from the Refresher

The refresher gives a simple example using a fruit list:

```python
fruits = ["apple", "banana", "cherry"]

fruits.append("orange")
print(fruits)

fruits.sort()
print(fruits)
```

After `append()`:

```text
['apple', 'banana', 'cherry', 'orange']
```

After `sort()`:

```text
['apple', 'banana', 'cherry', 'orange']
```

---

# Quick List Methods Table

| Method             | Purpose                          |
| ------------------ | -------------------------------- |
| `append(x)`        | Add one item at the end          |
| `extend(iterable)` | Add multiple items               |
| `insert(index, x)` | Add item at specific index       |
| `remove(x)`        | Remove first occurrence of value |
| `pop(index)`       | Remove and return element        |
| `index(x)`         | Find first index of value        |
| `count(x)`         | Count occurrences                |
| `sort()`           | Sort ascending                   |
| `reverse()`        | Reverse list order               |
| `copy()`           | Create shallow copy              |
| `clear()`          | Remove all elements              |

---

# Quick Revision

## Create List

```python
numbers = [1, 2, 3]
```

## Add One Element

```python
numbers.append(4)
```

## Add Multiple Elements

```python
numbers.extend([5, 6])
```

## Insert Element

```python
numbers.insert(1, 10)
```

## Remove by Value

```python
numbers.remove(10)
```

## Remove by Index

```python
numbers.pop(1)
```

## Find Index

```python
numbers.index(3)
```

## Count Value

```python
numbers.count(2)
```

## Sort

```python
numbers.sort()
```

## Reverse

```python
numbers.reverse()
```

## Copy

```python
new_numbers = numbers.copy()
```

## Empty List

```python
numbers.clear()
```

---

# Simple Flow

```text
Python List
    |
    ├── Add
    |    ├── append()
    |    ├── extend()
    |    └── insert()
    |
    ├── Remove
    |    ├── remove()
    |    ├── pop()
    |    └── clear()
    |
    ├── Search
    |    ├── index()
    |    └── count()
    |
    └── Organize
         ├── sort()
         ├── reverse()
         └── copy()
```

---

# Key Takeaways

* A list is an **ordered and mutable** collection.
* Lists can contain values of different data types.
* `append()` adds one element.
* `extend()` adds multiple elements.
* `insert()` adds an element at a specified position.
* `remove()` removes by value.
* `pop()` removes by index and returns the removed element.
* `index()` finds the position of a value.
* `count()` counts occurrences.
* `sort()` sorts the list.
* `reverse()` reverses its order.
* `copy()` creates a shallow copy.
* `clear()` removes all elements.