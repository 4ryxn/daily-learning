# Installing Anaconda on macOS

Anaconda is a Python distribution commonly used for **Data Science, Machine Learning, and scientific computing**.

It provides:

* Python
* Conda package manager
* Environment management
* Jupyter Notebook
* Common Data Science libraries

---

## Step 1: Check Your Mac Processor

Before downloading Anaconda, check whether your Mac uses:

* **Apple Silicon** — M1, M2, M3, M4, etc.
* **Intel Processor**

On macOS:

```text
Apple Menu → About This Mac
```

Download the installer that matches your Mac architecture.

> Current Anaconda installers primarily target Apple Silicon Macs; Intel-macOS support has changed, so always check the official download page before installing.

---

## Step 2: Download Anaconda

Download **Anaconda Distribution for macOS** from the official Anaconda website.

You can install it using either:

* Graphical installer
* Terminal installer

For beginners, the graphical installer is usually easier.

---

## Step 3: Install Anaconda

Open the downloaded installer and follow the installation steps.

Typical process:

```text
Download Installer
       ↓
Open Installer
       ↓
Accept License
       ↓
Select Installation Location
       ↓
Install Anaconda
       ↓
Initialize Conda
```

---

## Step 4: Open Terminal

After installation, open:

```text
Applications → Utilities → Terminal
```

macOS normally uses **zsh** as its default shell.

---

## Step 5: Check Conda Installation

Run:

```bash
conda --version
```

Example output:

```text
conda 26.x.x
```

If a version number appears, Conda is installed correctly.

---

## Step 6: Check Python

Run:

```bash
python --version
```

or:

```bash
python3 --version
```

---

## Step 7: Initialize Conda

If Conda is installed but not automatically available in your shell, run:

```bash
conda init zsh
```

Then either close and reopen Terminal or run:

```bash
source ~/.zshrc
```

`conda init` configures your shell so that Conda commands and environment activation work correctly.

---

## Step 8: Verify Conda

Run:

```bash
conda info
```

This displays information such as:

* Conda version
* Active environment
* Python version
* Installation path

---

## Useful Conda Commands

### Check Conda version

```bash
conda --version
```

### View environments

```bash
conda env list
```

### Create an environment

```bash
conda create -n myenv python=3.12
```

### Activate environment

```bash
conda activate myenv
```

### Deactivate environment

```bash
conda deactivate
```

---

## Key Takeaway

Installing Anaconda gives us a complete Python and Data Science setup containing **Conda, Python, Jupyter, and many commonly used packages**.

After installation, always verify it using:

```bash
conda --version
```
