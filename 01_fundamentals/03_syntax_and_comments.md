# 03: Syntax and Comments

This guide covers syntax rules in Python, including  comments, statements, indentation, case sensitivity, and common syntax errors.

---

## Comments

Comments are notes used to explain code and clarify logic. They are ignored by the Python interpreter.

Use the hash symbol `#` to start a **single-line comment**.

```python
GRAVITY = 9.81   # This is an single-line comment.
```

Use triple quotes, either `"""` or `'''`, for comments that span **multiple lines**.

```python
"""
This is a multi-line comment.
It can span several lines and is useful for
explaining complex logic.
"""
velocity = 27500
```

---

## Statements and Lines

A **statement** is a single instruction that the Python interpreter can execute. Typically, one statement is written per line.

```python
planet = "Mars"   # A single statement
print(planet)     # Another statement
```

If a statement is too long to fit on one line, it can be continued across multiple lines.

```python
# This long list is a single statement split across multiple lines
moons = [
    "Phobos", "Deimos", "Europa",
    "Ganymede", "Titan", "Callisto",
]
```

---

## Indentation

Python uses **indentation** to define a **block of code**, which is a group of statements that are executed together.

The standard convention is to use **four spaces** for each level of indentation.

```python
is_ready = True
if is_ready:
    print("This line is inside the if block")
    print("This is also inside the if block")

print("This line is outside the if block.")
```

**Note**: Mixing tabs and spaces can cause bugs. Configure the text editor to convert tabs to spaces to avoid issues.

---

## Case Sensitivity

Python is **case-sensitive**. This means that identifiers with different casing are treated as distinct and separate entities.

```python
mission = "Apollo"
Mission = "Gemini"
MISSION = "Artemis"


print(mission)   # Output: Apollo
print(Mission)   # Output: Gemini
```

---

## Syntax Errors

A **syntax error** occurs when Python code violates the language’s structural rules. When this happens, the interpreter stops and displays a `SyntaxError`, indicating that it doesn’t understand the code.

### Missing Indentation (`IndentationError`)
  
This happens when code blocks are not indented correctly.

```python
# This code will fail
is_ready = True
if is_ready:
print("The indentation is wrong!")
```

**Error**: `IndentationError: expected an indented block`

### Unexpected Indentation (`IndentationError`)

The opposite error occurs when a line of code is indented without a valid reason.

```python
# This code will fail
status = "Orbit achieved"
    print(status)
```

**Error**: `IndentationError: unexpected indent`

### Unterminated String (`SyntaxError`)

This happens when you start a string with a quote but forget to add the closing quote.

```python
# This code will fail
print("Liftoff initiated
```

**Error**: `SyntaxError: unterminated string literal`

