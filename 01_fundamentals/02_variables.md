# 02: Variables

This guide covers how to create, name, and use variables in Python.

---

## What is a Variable?

A **variable** is a named reference or pointer to a value stored in memory. It serves as a label for a piece of data.

You create a variable by choosing a name and assigning a value to it using the equals sign `=`. This is called an **assignment statement**.

```python
user_name = "Ada Lovelace"
user_age = 36
is_programmer = True
```

---

## Dynamic Typing

Python is a **dynamically typed** language. This means there is no need to specify the data type of a variable when creating it. The type is determined at **runtime** based on the assigned value.

You can also change the value and type stored in a variable at any time.

```python
user_age = 37
user_age = "thirty-seven"
```

---

## Naming Rules and Conventions

**Rules (required)**:
- A variable name must start with a letter (`a-z`, `A-Z`) or an underscore (`_`).
- It cannot start with a number.
- It can only contain letters, numbers, and underscores.
- Variable names are case-sensitive (`age`, `Age`, and `AGE` are three different variables).

**Conventions (highly recommended via PEP 8)**:
- Use `snake_case` for variable names (all lowercase words separated by underscores).
- Choose descriptive names that clearly communicate the variable's purpose.

**Good Names**: first_name, user_input, total_price   
**Bad Names**: FirstName, u, totalprice, 1st_name

---

## Constants

A **constant** is a type of variable whose value is not meant to be changed. Python doesn't have a strict rule to enforce this, but the universal convention is to name constants in all `UPPERCASE_WITH_UNDERSCORES`.

```python
PI = 3.14159
TAX_RATE = 0.08875
```

---

## Runtime Errors and Tracebacks

An error that happens while a program is running is called a **runtime error**. When this occurs, Python will stop and display a message called a **traceback**.

One common runtime error is the `NameError`. This error happens when you try to use a variable that doesn't exist, often because of a typo.

```python
message = "This is a test."
print(mesage)
```

Because `message` was misspelled as `mesage`, Python doesn't recognize the variable. It will stop and display a traceback.

```bash
Traceback (most recent call last):
  File "/path/to/your/file.py", line 2, in <module>
    print(mesage)
NameError: name 'mesage' is not defined
```

**How to Read a Traceback**:
- **File and Line Number**: `File "/path/to/your/file.py", line 2` tells you exactly where the error occurred.
- **The Failing Code**: Highlights the line that caused the crash: `print(mesage)`.
- **The Error Type**: `NameError` tells you what kind of error it is.
- **The Error Message**: `name 'mesage' is not defined` explains specifically what went wrong.
