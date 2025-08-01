# 03: Syntax and Comments

This guide covers Python's syntax, including how to structure code and leave comments.

---

## Comments

**Comments** are notes used to explain code and clarify logic. They are ignored by the Python interpreter.

### Single-line comments

To write a comment that fits on a single line, use the hash symbol (`#`).

```python
planet = "Saturn" # This is an single-line comment.
```

### Multi-line comments

For comments that span multiple lines, enclose the text in triple quotes (`"""` or `'''`).

```python
"""
This is a multi-line comment.
It can span several lines and is useful for
explaining complex logic.
"""
rings = 7
```

---

## Statements and Lines

A **statement** is a single instruction that the Python interpreter can execute. Typically, one statement is written per line.

```python
composition = "hydrogen"  # A single statement
print(composition)        # Another statement
```

Long statements can be split across multiple lines.

```python
# This long list is a single statement split across multiple lines
moons = [
    "Titan", "Enceladus", "Mimas",
    "Rhea", "Tethys", "Iapetus"
]
```

---

## Indentation

Python uses **indentation** to define a **block of code**, which is a group of statements that are executed together.

The standard is **four spaces** per indentation level.

```python
is_ready = True

if is_ready:
    # This indented block runs only if is_ready is True.
    print("This line is inside the if block")
    print("This is also inside the if block")

# This statement is not indented, so it always runs.
print("This line is outside the if block.")
```

*Note*: Mixing tabs and spaces can cause bugs. Configure the text editor to convert tabs to spaces to avoid issues.

---

## Case Sensitivity

Python is **case-sensitive**. This means that identifiers (like variable names) with different casing are treated as separate entities.

```python
# These are three different variables.
mission = "Cassini"
Mission = "Huygens"
MISSION = "Pioneer"

print(mission) # Output: Cassini
print(Mission) # Output: Huygens
```

---

## Syntax Errors

A **syntax error** occurs when Python code violates the language’s structural rules. When this happens, the interpreter stops and displays a `SyntaxError`, indicating that it doesn’t understand the code.

### Missing Indentation (`IndentationError`)
  
This syntax error happens when a line of code that requires indentation is missing it.

```python
# This code will fail
is_ready = True
if is_ready:
print("The indentation is wrong!")
```

Error: `IndentationError: expected an indented block`

### Unexpected Indentation (`IndentationError`)

This syntax error happens when a line of code is indented without a valid reason.

```python
# This code will fail
day_length = 10.7
    print(day_length)
```

Error: `IndentationError: unexpected indent`

### Unterminated String (`SyntaxError`)

This syntax error happens when a string has a starting quote but not a closing one.

```python
# This code will fail
print("Liftoff initiated
```

Error: `SyntaxError: unterminated string literal`

### Invalid Keyword (`SyntaxError`)

This syntax error happens when a reserved word is used incorrectly.

```python
# This code will fail
True = 1
```

Error: `SyntaxError: cannot assign to True`
