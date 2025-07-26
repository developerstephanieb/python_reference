# 02: Variables and Data Types

This guide introduces variables and the fundamental types of data they can hold.

---

## Variables

A **variable** is a named reference to a value stored in memory. It serves as a label for a piece of data.

Create a variable by choosing a name and assigning a value to it using the **assignment operator** (`=`).

```python
planet = "Earth"
continents = 7
```

---

## Dynamic Typing

Python is a **dynamically typed** language. This means variable types are determined when the program runs (**runtime**).

Variables can be **reassigned** to a different value and type.

```python
population = 8000000000
population = "Eight billion"
```

---

## Naming Variables and Constants

Python variables are named according to specific rules and conventions.

### Rules

Variable names must follow a set of syntactic rules to be valid.

- A variable name must start with a letter (`a-z`, `A-Z`) or an underscore (`_`).
- Cannot start with a number.
- Can only contain letters, numbers, and underscores.
- Names are case-sensitive (`sea`, `Sea`, and `SEA` are three different variables).

### Conventions (`PEP 8`)

Beyond the rules, the [PEP 8](https://peps.python.org/pep-0008/) style guide defines standard naming conventions.

- Use `snake_case` (all lowercase words separated by underscores).
- Choose short, descriptive names that clearly communicate the purpose.
- Good Names: `first_name`, `user_input`, `mph`   
- Bad Names: `FirstName`, `1st_name`, `u`, `milesperhour`

### Constants

A **constant** is a variable whose value is not meant to change. Python doesn't enforce this, but the convention is to name constants in `UPPERCASE_WITH_UNDERSCORES`.

```python
GRAVITY = 9.81
EARTH_RADIUS_KM = 6371
```

---

## Data Types

Every value in Python has a **data type**.

### Strings (`str`)

A **string** is a sequence of characters used to represent text. Create strings using single `'` or double `"` quotes.  It can contain one type of quotation mark when enclosed by the other. 

```python
country = "Brazil"
climate_fact = 'The Amazon is often called the "lungs of the Earth" because of its vast oxygen production.'
```

### Integers (`int`)

**Integers** are whole numbers. For large numbers, underscores can be used as visual separators to improve readability. Python ignores the underscores when storing the values.

```python
rainforest_types = 2
trees_in_amazon = 390_000_000_000
```

### Floats (`float`)

A **float**, or floating-point number, is a number with a decimal component.

```python
fuel_price = 12.95
rocket_price = 67_275_150_901.78
```

### Booleans (`bool`)

**Boolean** represent `True` or `False`.

```python
is_habitable = True
has_rings = False
```

---

## Checking a Variable's Type with `type()`

To determine the data type of a variable, use the built-in `type()` function. **Built-in functions** are tools provided as part of the language that can be used directly.

Syntax: `type(object)`

```python
spacecraft = "Voyager 1"
launch_year = 1977

print(type(spacecraft))
print(type(launch_year))
```

---

## Runtime Errors and Tracebacks

An error that occurs while a program is running is called a **runtime error**. When this happens, Python stops and displays a **traceback**, a message that explains where and why the error happened.

### `NameError`

A runtime error that occurs when a variable is used before it has been defined, often due to a typo.

```python
message = "Welcome to Earth"
print(mesage)
```

Because `message` was misspelled as `mesage`, Python doesn't recognize the variable. 

```bash
Traceback (most recent call last):
  File "/path/to/your/file.py", line 2, in <module>
    print(mesage)
NameError: name 'mesage' is not defined
```

### How to Read a Traceback

The traceback message helps identify and fix errors.

- **File and Line Number**: `File "/path/to/your/file.py", line 2` indicates where the error occurred.
- **The Failing Code**: `print(mesage)` displays the line that caused the crash.
- **The Error Type**: `NameError` specifies the error type.
- **The Error Message**: `name 'mesage' is not defined` details the cause of the error.
