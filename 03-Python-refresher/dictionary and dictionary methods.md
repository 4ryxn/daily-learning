# Dictionary and Dictionary Methods in Python

A **dictionary** in Python is a collection of **key-value pairs**.

Your refresher describes dictionaries as mutable collections that allow efficient retrieval and modification, and notes that dictionaries preserve insertion order in modern Python.

---

# Creating a Dictionary

Dictionaries are created using curly braces:

```python id="bb7m1i"
{}
```

with data stored in:

```text id="j8z2wm"
key : value
```

pairs.

---

## Empty Dictionary

```python id="jmz5at"
empty_dict = {}
```

---

## Dictionary with Key-Value Pairs

```python id="dkg18t"
student = {
    "name": "Alice",
    "age": 25,
    "grade": "A"
}
```

Here:

```text id="hr4ewq"
"name"  → key
"Alice" → value

"age"   → key
25      → value
```

The refresher uses this same `student` dictionary example.

---

# Creating a Dictionary Using `dict()`

A dictionary can also be created using the `dict()` constructor.

```python id="578mlx"
person = dict(
    name="John",
    age=30,
    city="New York"
)
```

---

# Accessing Dictionary Elements

Dictionary values are accessed using their keys.

Example:

```python id="qhptfu"
student = {
    "name": "Alice",
    "age": 25,
    "grade": "A"
}

print(student["name"])
```

Output:

```text id="ie8f56"
Alice
```

The refresher shows the same direct key-access example.

---

# Using `get()`

Another way to access a dictionary value is:

```python id="79jtsp"
student.get("age")
```

Example:

```python id="w7eo8w"
print(student.get("age"))
```

Output:

```text id="u4foz7"
25
```

The advantage of `get()` is that we can provide a default value if the key does not exist.

```python id="x23zgn"
print(student.get("height", "Not Found"))
```

Output:

```text id="jkwyh7"
Not Found
```

## The refresher specifically points out that `get()` avoids a `KeyError` when the key is missing.

# Adding a New Key-Value Pair

A new item can be added using:

```python id="lo918s"
dictionary[key] = value
```

Example from the refresher:

```python id="bjxi0u"
student["city"] = "New York"
```

Now:

```python id="m6mu6n"
print(student)
```

contains the new `city` key.

---

# Updating an Existing Value

We can change a value using its key.

```python id="7xuwvn"
student["age"] = 26
```

The key already exists, so Python updates its value.

---

# Common Dictionary Methods

The refresher covers these methods:

```text id="fol179"
keys()
values()
items()
get()
update()
pop()
popitem()
setdefault()
clear()
copy()
```

---

# 1. `keys()`

`keys()` returns all the keys in the dictionary.

```python id="wsm0ye"
student = {
    "name": "Alice",
    "age": 25,
    "grade": "A"
}

print(student.keys())
```

It contains keys such as:

```text id="n3usrn"
name
age
grade
```

Syntax:

```python id="3hpwr3"
dictionary.keys()
```

---

# 2. `values()`

`values()` returns all values in the dictionary.

```python id="9axnga"
print(student.values())
```

The values are:

```text id="pzmgbd"
Alice
25
A
```

Syntax:

```python id="zu4mej"
dictionary.values()
```

---

# 3. `items()`

`items()` returns dictionary key-value pairs as tuples.

```python id="b9c8gz"
print(student.items())
```

Conceptually:

```text id="w2vbyc"
("name", "Alice")
("age", 25)
("grade", "A")
```

Syntax:

```python id="k26299"
dictionary.items()
```

---

# Iterating Over a Dictionary

`items()` is especially useful with loops.

Example from the refresher:

```python id="ef1a2j"
student = {
    "name": "Alice",
    "age": 26,
    "city": "New York"
}

for key, value in student.items():
    print(key, ":", value)
```

Output:

```text id="3rczar"
name : Alice
age : 26
city : New York
```

---

# 4. `get()`

`get()` returns the value associated with a key.

Syntax:

```python id="esjlxt"
dictionary.get(key, default)
```

Example:

```python id="7ld9rj"
student.get("age", 0)
```

If `"age"` exists, its value is returned.

If it does not exist, the default value `0` is returned.

---

# 5. `update()`

`update()` merges another dictionary into the existing dictionary.

Example from the refresher:

```python id="b5gcsb"
student.update({
    "age": 26
})
```

This updates the value of `"age"`.

Syntax:

```python id="svmk3c"
dictionary.update(other_dictionary)
```

---

# 6. `pop()`

`pop()` removes a key and returns its value.

Example:

```python id="d15gpn"
student.pop("grade")
```

After this, the `"grade"` key is removed.

Syntax:

```python id="dt5a10"
dictionary.pop(key, default)
```

If a default is provided, it can be returned when the key does not exist.

---

# 7. `popitem()`

`popitem()` removes and returns the **last inserted key-value pair**.

Example:

```python id="5j0qmf"
student.popitem()
```

Syntax:

```python id="jppr57"
dictionary.popitem()
```

---

# `pop()` vs `popitem()`

```text id="yexlzv"
pop(key)
   ↓
Remove a specific key
```

```text id="y491ng"
popitem()
   ↓
Remove the last inserted key-value pair
```

---

# 8. `setdefault()`

`setdefault()` returns the value of a key if the key already exists.

If it does not exist, the key is added with a default value.

Example from the refresher:

```python id="3yjvfz"
student.setdefault("city", "Unknown")
```

If `"city"` exists:

```text id="ks8355"
Return its current value
```

If `"city"` does not exist:

```text id="91r3y8"
Add:

"city": "Unknown"
```

---

# 9. `clear()`

`clear()` removes all items from a dictionary.

```python id="3q3jpk"
student.clear()
```

After this:

```python id="nn19wg"
print(student)
```

Output:

```text id="h1zrpm"
{}
```

---

# 10. `copy()`

`copy()` creates a shallow copy of a dictionary.

```python id="8jcvzg"
new_dict = student.copy()
```

Now `new_dict` contains a copy of the dictionary.

---

# Key Properties of Dictionaries

The refresher highlights three important properties:

* Dictionaries preserve insertion order in modern Python.
* Keys must be **unique and immutable**.
* Values can be mutable and can contain different data types.

Examples of valid key types include:

```text id="5ebudn"
Strings
Numbers
Tuples
```

---

# Unique Keys

A dictionary cannot have duplicate keys representing separate items.

For example:

```python id="obyub2"
student = {
    "name": "Alice",
    "name": "Bob"
}
```

The same key cannot represent two separate entries.

The refresher specifically states that dictionary keys must be unique.

---

# Dictionary Comprehension

The refresher also introduces **dictionary comprehension**.

It allows dictionaries to be created in a concise form.

Example:

```python id="vxsn5d"
squares = {
    x: x**2
    for x in range(1, 6)
}

print(squares)
```

Output:

```text id="x6p5dn"
{
    1: 1,
    2: 4,
    3: 9,
    4: 16,
    5: 25
}
```

Basic syntax:

```python id="82l9xd"
{key_expression: value_expression for item in iterable}
```

---

# Dictionary Methods Summary

| Method         | Purpose                                 |
| -------------- | --------------------------------------- |
| `keys()`       | Return all keys                         |
| `values()`     | Return all values                       |
| `items()`      | Return key-value pairs                  |
| `get()`        | Get value safely                        |
| `update()`     | Merge/update dictionary                 |
| `pop()`        | Remove a specific key                   |
| `popitem()`    | Remove last inserted pair               |
| `setdefault()` | Get key or create it with default value |
| `clear()`      | Remove all items                        |
| `copy()`       | Create shallow copy                     |

---

# Quick Revision

## Create Dictionary

```python id="32hvkm"
student = {
    "name": "Alice",
    "age": 25
}
```

## Access Value

```python id="o8mrtd"
student["name"]
```

## Safe Access

```python id="r1o9d5"
student.get("name")
```

## Add New Item

```python id="kmie2x"
student["city"] = "New York"
```

## Update Item

```python id="93si1h"
student["age"] = 26
```

## Get Keys

```python id="ydyy7g"
student.keys()
```

## Get Values

```python id="zlq1up"
student.values()
```

## Get Key-Value Pairs

```python id="ecol3k"
student.items()
```

## Remove Specific Key

```python id="vub1cp"
student.pop("age")
```

## Remove Last Pair

```python id="yjzet9"
student.popitem()
```

## Copy Dictionary

```python id="atb4ni"
new_dict = student.copy()
```

## Clear Dictionary

```python id="rb4nt2"
student.clear()
```

---

# Simple Flow

```text id="mjzi6j"
Dictionary
    |
    ├── Access
    |    ├── [key]
    |    └── get()
    |
    ├── View
    |    ├── keys()
    |    ├── values()
    |    └── items()
    |
    ├── Modify
    |    ├── update()
    |    └── setdefault()
    |
    ├── Remove
    |    ├── pop()
    |    ├── popitem()
    |    └── clear()
    |
    └── Copy
         └── copy()
```

---

# Key Takeaways

* Dictionaries store data as **key-value pairs**.
* Keys must be unique.
* Values can contain different kinds of data.
* Dictionary values can be accessed using `dictionary[key]` or `get()`.
* `keys()`, `values()`, and `items()` are used to inspect dictionary data.
* `update()` changes or merges data.
* `pop()` removes a specified key.
* `popitem()` removes the last inserted pair.
* `setdefault()` returns an existing value or creates a key with a default value.
* `clear()` empties the dictionary.
* `copy()` creates a shallow copy.
