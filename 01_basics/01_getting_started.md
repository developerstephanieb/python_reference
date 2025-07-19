# 01: Getting Started with Python

This guide covers the essentials of installing Python and running code.

---

## Installing Python

To run Python code, the Python **interpreter** must be installed.

### Installation Methods

Python can be installed from the official source or via a package manager.

- **Official source (All Platforms)**  
 
   Download the latest version from the official website: [python.org/downloads](https://www.python.org/downloads/)

- **macOS (via Homebrew)**  

  Use the [`Homebrew`](https://brew.sh) package manager. In a terminal, run:  

   ```bash
   brew install python3
   ```

- **Linux (Debian/Ubuntu)**   

  Most Linux distributions come with Python pre-installed.

  If not, use the `apt` package manager. In a terminal, run:

   ```bash
   sudo apt install python3
   ```

### 2. Verify Installation

Confirm the installation was successful by running:

```bash
python3 --version
```

This should display the installed Python version, such as `Python 3.12.4`.

---

## Running Python Code

There are two primary ways to run Python code: interactively in a REPL or by executing a script file.

### 1. Interactive Mode (REPL)

The **REPL** (Read–Eval–Print Loop) is an tool for testing small code snippets directly in the terminal.

- **Launch the interpreter** by opening a terminal and running:

   ```bash
   python3
   ```

   The prompt `>>>` will appear, indicating the interpreter is ready for input.

- Enter a command directly into the prompt:

   ```bash
   >>> print("Hello, World!")
   ```

   Python will execute the code and print `Hello, World!` to the console.

- To exit the session, type `exit()`.

### 2. Script File Execution

For larger programs, save your code in a file with a `.py` extension and run it from the terminal.

- **Create a file** named `hello.py` using a text editor or IDE like [VS Code](https://code.visualstudio.com). 
   
- **Write your code** inside the file and **save** it:

   ```python
   print("Hello, World!")
   ```

- **Navigate to the file's directory** in the terminal:
  
  ```bash
  cd path/to/hello.py
  ```

- **Run the script** by using the `python3` command followed by the filename:

   ```bash
   python3 hello.py
   ```

   The program will execute and print `Hello, World!` to the terminal.
