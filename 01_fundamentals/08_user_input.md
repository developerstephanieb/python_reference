# 09: User Input

This guide outlines how to prompt for and handle user input.

---

## The `input()` Function

The built-in `input()` function is the primary way to get user input. When called, it pauses the program and waits for the user to type some text and press the Enter key.

The text that the user types is then returned by the function as a string, which you can store in a variable.

```python
# The program will pause here and wait for the user to type their name
print("What is your name?")
name = input()

print("Hello, " + name + "!")
```

---

## Providing a Prompt

It's much more user-friendly to display a message, or prompt, that tells the user what to enter. To do this, pass a string to the `input()` function to display it as a prompt.

```python
# The string passed to input() is displayed as a prompt
name = input("Please enter your name: ")
print("Welcome, " + name + "!")
```

---

## Type Errors

The `input()` function always returns the user's input as a string, even if they type in numbers.

A **type error** occurs when an operation is performed on a value of the wrong type. When this happens, the interpreter stops and displays a `TypeError`.

### Mixing Strings and Integers (`TypeError`)

```python
# This code will cause an error
age_string = input("How old are you? ")

# You can't add an integer to a string
age_in_ten_years = age_string + 10 
```

**Error**: `TypeError: can only concatenate str (not "int") to str`

---

## Converting Input to the Correct Type

To use the user's input as a number, it must first be converted from a string to the correct data type. This can be done using the built-in `int()` and `float()` functions.

### `int()`

To convert from a string to an integer, use the built-in `int()` function.

Syntax: `int(value, base)`

| Parameter | Required? | Description                                       | Default |
| :-------: | :-------: | ------------------------------------------------- | :-----: |
|   value   |    Yes    | The value to convert to an integer                |    -    |
|   base    |    No     | The numeric base (e.g., 2 for binary, 16 for hex) |   10    |

```python
# Get the user's age as a string
age_string = input("How old are you? ")

# Convert the string to an integer
age_integer = int(age_string)

# Now you can perform math with it
age_in_ten_years = age_integer + 10
print("In ten years, you will be", age_in_ten_years, "years old.")
```

It is common to combine these steps into a single line:

```python
# Get input and immediately convert it to an integer
age = int(input("How old are you? "))
```

### `float()`

to convert a string to an floating-point number, use the built-in `float()` function.

Syntax: `float(value)`

```python
height = float(input("Enter your height in meters: "))
```
