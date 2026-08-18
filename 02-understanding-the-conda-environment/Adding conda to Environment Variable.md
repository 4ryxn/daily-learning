# Adding Conda to Environment Variables on macOS

## What are Environment Variables?

Environment variables store information that programs and the operating system can use.

One important environment variable is:

```text
PATH
```

`PATH` tells the Terminal **where to search for executable programs**.

For example, when we type:

```bash
python
```

or:

```bash
conda
```

the shell searches directories listed inside `PATH`.

---

# Why Does Conda Need PATH Configuration?

Sometimes Anaconda is installed correctly, but Terminal may show:

```text
command not found: conda
```

This usually means the shell has not been configured to locate or initialize Conda.

---

# Recommended Method: conda init

On modern Conda installations, manually editing `PATH` is usually unnecessary.

Instead run:

```bash
conda init zsh
```

Since modern macOS normally uses **zsh**, this modifies your shell configuration.

Then reload it:

```bash
source ~/.zshrc
```

Or simply close and reopen Terminal.

---

# What is `.zshrc`?

`.zshrc` is a configuration file used by the **zsh shell**.

Its location is:

```text
~/.zshrc
```

The `~` represents your home directory.

For example:

```text
/Users/username/.zshrc
```

When Terminal starts, zsh reads this file and applies its configuration.

---

# Check Which Shell You Are Using

Run:

```bash
echo $SHELL
```

Example:

```text
/bin/zsh
```

This means you are using **zsh**.

---

# Check Whether Conda is Available

Run:

```bash
which conda
```

Example output may point to your Conda installation.

You can also run:

```bash
conda --version
```

---

# If `conda init` Cannot Be Run

If Conda has been installed but your shell cannot find it, first activate Conda directly using its installation path.

For a common Anaconda installation:

```bash
source ~/anaconda3/bin/activate
```

Then run:

```bash
conda init zsh
```

Finally:

```bash
source ~/.zshrc
```

---

# Understanding PATH

You can display your current PATH using:

```bash
echo $PATH
```

It may look similar to:

```text
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

Each directory is separated using:

```text
:
```

---

# Manual PATH Method

Manual PATH editing should generally be used only when necessary.

For example:

```bash
export PATH="$HOME/anaconda3/bin:$PATH"
```

This can be added to:

```text
~/.zshrc
```

However, **`conda init zsh` is preferred**, because Conda environment activation requires more than simply finding the `conda` executable.

---

# Why `conda init` is Better

`conda init` configures the shell so commands such as:

```bash
conda activate myenv
```

work correctly.

It also updates the shell configuration needed for Conda environment activation.

---

# Useful Commands

### Check shell

```bash
echo $SHELL
```

### Check PATH

```bash
echo $PATH
```

### Find Conda

```bash
which conda
```

### Initialize Conda

```bash
conda init zsh
```

### Reload configuration

```bash
source ~/.zshrc
```

### Check Conda

```bash
conda --version
```

---

# Quick Flow

```text
Install Anaconda
      ↓
Open Terminal
      ↓
conda --version
      ↓
If Conda is not initialized
      ↓
conda init zsh
      ↓
source ~/.zshrc
      ↓
Conda Ready
```

## Key Takeaway

On macOS, you normally **do not need to manually add Anaconda to PATH**.

The recommended approach is:

```bash
conda init zsh
source ~/.zshrc
```

This configures Conda properly for the zsh shell and allows environments to be activated from Terminal.
