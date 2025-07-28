# 01: Getting Started

This guide covers the essentials of installing Python and running code.

---

## Installing Python

To write and run Python code, first install the Python **interpreter**, which is the program that reads and executes the code.

### Installation Methods

Python can be installed from the official source or via a package manager.

- **Official source (All Platforms)**  
 
   Download the latest version from the official website: [python.org/downloads](https://www.python.org/downloads/)

- **macOS (via [`Homebrew`](https://brew.sh))**  

  In a terminal, run:

   ```bash
   brew install python3
   ```

- **Linux (Debian/Ubuntu)**   

  In a terminal, run:

   ```bash
   sudo apt install python3
   ```

### Verifying the Installation

Confirm that the installation was successful by checking the installed Python version.

In a terminal, run:

```bash
python3 --version
```

A successful installation will display the installed Python version, such as `Python 3.12.4`.

---

## Running Python Code

There are two primary ways to run Python code: interactively in a REPL or by executing a script file.

### Interactive Mode (REPL)

The **REPL** (Read–Eval–Print Loop) is an tool for testing small code snippets directly in the terminal.

1. Launch the interpreter by running `python3`. The prompt (`>>>`) will appear.

   ```bash
   python3
   ```

2. Enter a command directly into the prompt.

   ```bash
   >>> print("Hello, World!")
   ```

The interpreter will print `Hello, World!` to the terminal. To exit, enter `exit()`.

### Script File Execution

For code that needs to be saved, use a script file.

1. Create a file named `hello.py` using a text editor or IDE like [VS Code](https://code.visualstudio.com). All Python files must use the `.py` extension. 
   
2. Add code to the file and save it:

   ```python
   print("Hello, World!")
   ```

3. Navigate to the file's directory in the terminal:
  
   ```bash
   cd path/to/hello.py
   ```

1. Run the script from the terminal using the `python3` command followed by the filename:

   ```bash
   python3 hello.py
   ```

The program will print `Hello, World!` to the terminal.

