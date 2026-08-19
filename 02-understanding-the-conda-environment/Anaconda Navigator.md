# Anaconda Navigator - Quick Tour

Anaconda Navigator is a **Graphical User Interface (GUI)** included with Anaconda.

It allows us to work with Conda tools without using Terminal commands for every task.

---

# Opening Anaconda Navigator

On macOS, open:

```text
Applications → Anaconda Navigator
```

You can also start it from Terminal:

```bash
anaconda-navigator
```

---

# Main Features

Anaconda Navigator allows us to:

* Launch Jupyter Notebook
* Launch JupyterLab
* Manage Conda environments
* Install packages
* Update packages
* Remove packages
* Open development tools

---

# 1. Home Tab

The **Home** section displays applications available in Anaconda.

Common applications include:

* Jupyter Notebook
* JupyterLab
* Spyder

Each application usually has a:

```text
Launch
```

button.

---

# 2. Launching Jupyter Notebook

Find:

```text
Jupyter Notebook
```

Then click:

```text
Launch
```

It opens Jupyter Notebook in your browser.

---

# 3. Launching JupyterLab

Find:

```text
JupyterLab
```

Click:

```text
Launch
```

JupyterLab opens in the browser with a more advanced interface than classic Jupyter Notebook.

---

# 4. Environments Tab

The **Environments** section is used to manage Conda environments.

You can:

* Create environments
* Delete environments
* Install packages
* Update packages
* View installed packages

---

## Creating an Environment

Go to:

```text
Environments
      ↓
Create
```

Enter:

```text
Environment Name
Python Version
```

Example:

```text
Name: data-science
Python: 3.12
```

Then create the environment.

---

# 5. Selecting an Environment

The environments panel may contain entries such as:

```text
base
data-science
ml-project
```

Select an environment to manage its packages.

---

# 6. Installing Packages

Select an environment.

Then change the package filter from:

```text
Installed
```

to:

```text
Not installed
```

Search for a package.

Example:

```text
pandas
```

Select the package and apply the changes.

---

# 7. Updating Packages

Select:

```text
Updatable
```

Choose the package you want to update and apply the changes.

---

# 8. Removing Packages

Select the installed package and choose the remove option.

Then apply the changes.

---

# Navigator vs Terminal

The same task can often be performed either way.

### Navigator

```text
Create Environment → Click buttons
```

### Terminal

```bash
conda create -n myenv python=3.12
```

---

## Which Should You Use?

### Anaconda Navigator

Good for:

* Beginners
* Visual environment management
* Quick package installation
* Launching Jupyter

### Terminal

Better for:

* Developers
* Automation
* Faster workflows
* Reproducible commands
* Remote systems

---

# Simple Navigator Workflow

```text
Open Anaconda Navigator
        ↓
Select/Create Environment
        ↓
Install Required Packages
        ↓
Launch Jupyter
        ↓
Start Coding
```

## Key Takeaway

Anaconda Navigator provides a **GUI-based way to manage Conda environments and Data Science tools**.

It is useful for beginners, while Terminal commands provide more control and are more commonly used in development workflows.
