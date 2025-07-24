# 02: Variables and Data Types

This guide introduces Python variables, data types, naming rules, and how to troubleshoot common runtime errors.

---

## What is a Variable?

A **variable** is a named reference to a value stored in memory. It serves as a label for a piece of data.

You create a variable by choosing a name and assigning a value to it using the **assignment operator** `=`.

```python
planet = "Earth"
continents = 7
```

---

## Dynamic Typing

Python is a **dynamically typed** language, meaning you don't have to declare a variable's data type when creating it. The type is automatically determined when the program runs (**runtime**).

You can **reassign** a variable to a different value and type at any time.

```python
population = 8000000000
population = "Eight billion"
```

---

## Naming Variables and Constants

Good naming makes code easier to read and maintain.

### Rules

Variable names in Python must follow a set of syntactic rules to be valid.

- A variable name must start with a letter (`a-z`, `A-Z`) or an underscore (`_`).
- It cannot start with a number.
- It can only contain letters, numbers, and underscores.
- Variable names are case-sensitive (`sea`, `Sea`, and `SEA` are three different variables).

### Conventions

Beyond the rules, developers follow a set of common naming conventions.

- Use `snake_case` for variable names (all lowercase words separated by underscores).
- Choose short, descriptive names that clearly communicate the variable's purpose.
- Good Names: `first_name`, `user_input`, `mph`   
- Bad Names: `FirstName`, `1st_name`, `u`, `milesperhour`

### Constants

A **constant** is a type of variable whose value is not meant to be changed. Python doesn't have rules to enforce this, but the universal convention is to name constants in all `UPPERCASE_WITH_UNDERSCORES`.

```python
GRAVITY = 9.81
EARTH_RADIUS_KM = 6371
```

---

## Data Types

Every value belongs to a specific data type.

### Strings (`str`)

A **string** is a sequence of characters used to represent text. You create them using single `'` or double `"` quotes. You can also use both within a single string.

```python
country = "Brazil"
climate_fact = 'The Amazon is often called the "lungs of the Earth" because of its vast oxygen production.'
```

### Integers (`int`)

**Integers** are whole numbers. You can group digits using underscores to make large numbers more readable. Python ignores the underscores when storing the values.

```python
rainforest_types = 3
trees_in_amazon = 390_000_000_000
```

### Floats (`float`)

A **float**, or floating-point number, is a number with a decimal component.

```python
average_temperature = 14.9
surface_water_percent = 70.8
```

### Booleans (`bool`)

A **boolean** represents one of two values: `True` or `False`. Booleans are essential for logic and control flow. Note that `True` and `False` must be capitalized.

```python
is_habitable = True
has_rings = False
```

---

## Runtime Errors and Tracebacks

An error that occurs while a program is running is called a **runtime error**. When this happens, Python stops and displays a **traceback**, a message that explains where and why the error happened.

### `NameError`

One common runtime error is the `NameError`. This error happens when you try to use a variable that doesn't exist, often because of a typo.

```python
message = "Welcome to Earth"
print(mesage)
```

Because `message` was misspelled as `mesage`, Python doesn't recognize the variable. It stops and displays a traceback.

```bash
Traceback (most recent call last):
  File "/path/to/your/file.py", line 2, in <module>
    print(mesage)
NameError: name 'mesage' is not defined
```

### How to Read a Traceback

Understanding a traceback helps identify and fix errors.

- **File and Line Number**: `File "/path/to/your/file.py", line 2` tells you exactly where the error occurred.
- **The Failing Code**: Highlights the line that caused the crash: `print(mesage)`.
- **The Error Type**: `NameError` tells you what kind of error it is.
- **The Error Message**: `name 'mesage' is not defined` explains specifically what went wrong.
