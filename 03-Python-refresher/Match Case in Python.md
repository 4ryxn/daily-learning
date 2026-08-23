# Match Case in Python

The `match-case` statement is used for **pattern matching** in Python.

It was introduced in **Python 3.10** and works similarly to a `switch` statement found in some other programming languages.

---

# Basic Syntax

```python id="9fxn7q"
match value:
    case pattern1:
        # code
    case pattern2:
        # code
    case _:
        # default case
```

Python compares the value with each `case` pattern.

The first matching case is executed.

---

# Simple Example

Your refresher uses an HTTP status code example:

```python id="emsmce"
def http_status(code):
    match code:
        case 200:
            return "OK"

        case 400:
            return "Bad Request"

        case 404:
            return "Not Found"

        case 500:
            return "Internal Server Error"

        case _:
            return "Unknown Status"
```

Example:

```python id="c7f518"
print(http_status(200))
print(http_status(404))
```

Output:

```text id="mkcy5l"
OK
Not Found
```

This follows the same structure shown in the refresher.

---

# The `_` Default Case

The underscore:

```python id="sxu67j"
_
```

acts as the **default case**.

It runs when no previous pattern matches.

Example:

```python id="v6zho2"
status = 999

match status:
    case 200:
        print("OK")

    case 404:
        print("Not Found")

    case _:
        print("Unknown Status")
```

Output:

```text id="3yu8bm"
Unknown Status
```

Your refresher specifically notes that `_` acts as the default case.

---

# Match Case vs If-Elif-Else

The same logic can often be written using either approach.

## Using `if-elif-else`

```python id="ps9uja"
code = 404

if code == 200:
    print("OK")

elif code == 400:
    print("Bad Request")

elif code == 404:
    print("Not Found")

else:
    print("Unknown Status")
```

---

## Using `match-case`

```python id="1pp2qx"
code = 404

match code:
    case 200:
        print("OK")

    case 400:
        print("Bad Request")

    case 404:
        print("Not Found")

    case _:
        print("Unknown Status")
```

For several fixed values, `match-case` can make the code easier to read.

---

# Matching Data Structures

`match-case` can do more than compare simple values.

Your refresher shows pattern matching with a tuple.

Example:

```python id="y8km3h"
point = (3, 4)

match point:
    case (0, 0):
        print("Origin")

    case (x, 0):
        print(f"X-Axis at {x}")

    case (0, y):
        print(f"Y-Axis at {y}")

    case (x, y):
        print(f"Point at ({x}, {y})")
```

Output:

```text id="zp02lt"
Point at (3, 4)
```

---

# Understanding the Tuple Example

Suppose:

```python id="17rnw6"
point = (0, 5)
```

Python checks the cases in order.

### Case 1

```python id="rlfk79"
case (0, 0):
```

Does not match.

### Case 2

```python id="d169zy"
case (x, 0):
```

Does not match because the second value is not `0`.

### Case 3

```python id="68a2ok"
case (0, y):
```

Matches.

Here:

```text id="a5olil"
y = 5
```

So the output becomes:

```text id="67zd4x"
Y-Axis at 5
```

---

# Variable Binding

Patterns can capture values into variables.

Example:

```python id="ezyh5m"
point = (5, 0)

match point:
    case (0, 0):
        print("Origin")

    case (x, 0):
        print(f"X-Axis at {x}")
```

Here Python matches:

```python id="b77rx9"
(x, 0)
```

and assigns:

```text id="1oxgwe"
x = 5
```

Output:

```text id="rwmd51"
X-Axis at 5
```

The refresher notes that patterns can include **literals, variable bindings, and structural patterns**.

---

# Match Case Flow

```text id="814d7w"
Value
  ↓
match
  ↓
Check case 1
  ↓
Match?
 ├── Yes → Execute
 └── No
       ↓
   Check case 2
       ↓
     Match?
     ├── Yes → Execute
     └── No
           ↓
        case _
           ↓
       Default
```

---

# When to Use Match Case

`match-case` is useful when:

* Comparing one value against several fixed patterns
* Working with structured data
* Matching tuples
* Handling status codes
* Replacing long `if-elif-else` chains in suitable cases

---

# Quick Revision

```python id="m1yf1k"
match value:
    case pattern1:
        code

    case pattern2:
        code

    case _:
        default_code
```

Remember:

```text id="b0j8tg"
match → value to check

case → pattern to match

_ → default case
```

---

# Key Takeaway

`match-case` provides a clean way to perform **pattern matching** in Python.

Unlike a basic `if-elif-else`, it can also match structured patterns such as tuples and bind matched values to variables.

The most important thing to remember is:

```text id="2ovy4n"
match
  ↓
case
  ↓
first matching pattern executes
  ↓
case _ = default
```
