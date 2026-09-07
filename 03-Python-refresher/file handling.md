# File Handling in Python

**File handling** allows Python programs to **read, write, and manipulate files stored on disk**.

Python provides built-in functions for working with files.

---

# Opening a File

Python uses the `open()` function to open a file.

## Syntax

```python id="5p4h1e"
file = open("filename", mode)
```

Here:

```text id="l4bg7z"
filename → Name/path of the file
mode     → How the file should be opened
```

---

# File Modes

Python provides different modes depending on what we want to do with the file.

| Mode  | Meaning     |
| ----- | ----------- |
| `"r"` | Read        |
| `"w"` | Write       |
| `"a"` | Append      |
| `"x"` | Create      |
| `"b"` | Binary mode |
| `"t"` | Text mode   |

---

# 1. Read Mode `"r"`

`"r"` opens a file for reading.

It is also the **default mode**.

```python id="ct0ss1"
file = open("example.txt", "r")
```

If the file does not exist, Python raises an error.

---

# 2. Write Mode `"w"`

`"w"` opens a file for writing.

```python id="0wf6av"
file = open("example.txt", "w")
```

Important behavior:

```text id="5tdood"
File exists
   ↓
Existing content is overwritten

File does not exist
   ↓
New file is created
```

---

# 3. Append Mode `"a"`

Append mode adds new content **without deleting existing content**.

```python id="4rqz5l"
file = open("example.txt", "a")
```

If the file does not exist, a new file is created.

---

# 4. Create Mode `"x"`

`"x"` creates a new file.

```python id="52o420"
file = open("example.txt", "x")
```

If the file already exists, Python raises an error.

---

# 5. Binary Mode `"b"`

Binary mode is used for non-text files such as:

```text id="gy1z7x"
Images
PDFs
Other binary files
```

Examples:

```python id="etgo7c"
"rb"
"wb"
"ab"
```

---

# 6. Text Mode `"t"`

Text mode is used for normal text files.

It is the default mode.

Examples:

```python id="1fxg5y"
"rt"
"wt"
```

---

# Reading Files

The refresher covers three common methods:

```text id="5opjb3"
read()
readline()
readlines()
```

---

# 1. `read()`

`read()` reads the **entire file content**.

```python id="5wt7ch"
file = open("example.txt", "r")

content = file.read()

print(content)

file.close()
```

---

# 2. `readline()`

`readline()` reads **one line at a time**.

```python id="olc51r"
file = open("example.txt", "r")

line1 = file.readline()

print(line1)

file.close()
```

---

# 3. `readlines()`

`readlines()` reads all lines and returns them as a **list**.

```python id="8obgbq"
file = open("example.txt", "r")

lines = file.readlines()

print(lines)

file.close()
```

Example file:

```text id="fq88to"
Hello
Python
File Handling
```

`readlines()` gives something like:

```python id="eeaa6d"
[
    "Hello\n",
    "Python\n",
    "File Handling\n"
]
```

---

# `read()` vs `readline()` vs `readlines()`

| Method        | Purpose                    |
| ------------- | -------------------------- |
| `read()`      | Read entire file           |
| `readline()`  | Read one line              |
| `readlines()` | Read all lines into a list |

The same distinction is summarized in the refresher.

---

# Writing to Files

Python mainly uses:

```text id="4b2arw"
write()
writelines()
```

---

# 1. `write()`

`write()` writes content into a file.

Example:

```python id="nu669w"
file = open("example.txt", "w")

file.write("Hello, World!")

file.close()
```

Because the file is opened using `"w"`, existing content is overwritten.

---

# 2. `writelines()`

`writelines()` writes multiple strings to a file.

Example from the refresher:

```python id="qypmmn"
lines = [
    "Hello\n",
    "Welcome to Python\n",
    "File Handling\n"
]

file = open("example.txt", "w")

file.writelines(lines)

file.close()
```

Notice the use of:

```python id="c8wzii"
\n
```

which creates a new line.

---

# Appending to a File

Use `"a"` when you want to add content without removing existing data.

Example:

```python id="gszdsy"
file = open("example.txt", "a")

file.write("\nThis is an additional line.")

file.close()
```

The refresher explains that append mode adds content while preserving previous data.

---

# `write()` vs Append Mode

## Using `"w"`

```python id="5ccwt3"
file = open("example.txt", "w")
file.write("New Content")
file.close()
```

Existing content:

```text id="jfhcd5"
Old Content
```

becomes:

```text id="dd9rkk"
New Content
```

---

## Using `"a"`

```python id="4s9d8f"
file = open("example.txt", "a")
file.write("\nNew Content")
file.close()
```

Now:

```text id="5oozia"
Old Content
New Content
```

So remember:

```text id="45z2wb"
w → overwrite
a → append
```

---

# Closing a File

When using `open()` normally, the file should be closed after use.

```python id="pupcv0"
file.close()
```

Example:

```python id="hfrt95"
file = open("example.txt", "r")

content = file.read()

file.close()
```

The refresher explicitly reminds you to close the file after use.

---

# Using `with open()` — Best Practice

The refresher recommends using the `with` statement.

```python id="3zduyv"
with open("example.txt", "r") as file:
    content = file.read()

print(content)
```

The advantage is:

```text id="k9uy0k"
with open()
    ↓
Open file
    ↓
Perform operation
    ↓
File automatically closes
```

So there is no need to manually call:

```python id="brnrqn"
file.close()
```

---

# Writing Using `with open()`

```python id="u2aqsh"
with open("example.txt", "w") as file:
    file.write("Hello Python")
```

---

# Appending Using `with open()`

```python id="m5a9dz"
with open("example.txt", "a") as file:
    file.write("\nLearning File Handling")
```

Using `with` is generally cleaner because file closing is handled automatically.

---

# Checking Whether a File Exists

The refresher uses the `os` module to check whether a file exists.

```python id="t72lgd"
import os

if os.path.exists("example.txt"):
    print("File exists!")
else:
    print("File not found!")
```

---

# Deleting a File

The `os` module can also delete files.

```python id="o48hcc"
import os

if os.path.exists("example.txt"):
    os.remove("example.txt")
    print("File deleted.")
else:
    print("File does not exist.")
```

---

# Working with Binary Files

Binary files include files such as:

```text id="r5tj21"
.jpg
.png
.pdf
```

The refresher says these should be opened using binary mode `"b"`.

---

# Reading a Binary File

```python id="8pjv98"
with open("image.jpg", "rb") as file:
    data = file.read()

print(data)
```

`"rb"` means:

```text id="1qf7of"
r → read
b → binary
```

---

# Writing a Binary File

```python id="cw43ii"
with open("new_image.jpg", "wb") as file:
    file.write(data)
```

`"wb"` means:

```text id="dok9u9"
w → write
b → binary
```

---

# File Handling Flow

```text id="r9ctxw"
File Handling
      |
      ├── Open
      |    └── open()
      |
      ├── Read
      |    ├── read()
      |    ├── readline()
      |    └── readlines()
      |
      ├── Write
      |    ├── write()
      |    └── writelines()
      |
      ├── Append
      |    └── "a"
      |
      ├── Binary
      |    ├── "rb"
      |    └── "wb"
      |
      └── File Management
           ├── os.path.exists()
           └── os.remove()
```

---

# Quick Revision

## Open File

```python id="he4znb"
file = open("example.txt", "r")
```

## Read Entire File

```python id="ygtnsn"
file.read()
```

## Read One Line

```python id="cmp40t"
file.readline()
```

## Read All Lines as List

```python id="ny258f"
file.readlines()
```

## Write

```python id="r9e6tt"
file.write("Hello")
```

## Write Multiple Lines

```python id="q6edh8"
file.writelines(lines)
```

## Append

```python id="ij8tue"
with open("example.txt", "a") as file:
    file.write("\nMore text")
```

## Check File

```python id="x716o8"
os.path.exists("example.txt")
```

## Delete File

```python id="r5xszc"
os.remove("example.txt")
```

---

# File Modes Quick Table

| Mode  | Purpose                              |
| ----- | ------------------------------------ |
| `"r"` | Read existing file                   |
| `"w"` | Write and overwrite existing content |
| `"a"` | Add content at the end               |
| `"x"` | Create a new file                    |
| `"b"` | Binary mode                          |
| `"t"` | Text mode                            |

---

# Key Takeaways

* File handling lets Python read, write, and manipulate files.
* `open()` is used to open files.
* `"r"` reads files.
* `"w"` writes and overwrites content.
* `"a"` appends without removing existing content.
* `"x"` creates a new file.
* `read()`, `readline()`, and `readlines()` are used for reading.
* `write()` and `writelines()` are used for writing.
* `with open()` is the recommended approach because it automatically closes the file.
* `os.path.exists()` checks whether a file exists.
* `os.remove()` deletes a file.
* Binary files use modes such as `"rb"` and `"wb"`.
