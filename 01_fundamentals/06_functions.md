# 06: Functions

A **function** is a named, reusable block of code that performs a specific task.

---

## Defining and Calling a Function

To define a function, use the `def` keyword, followed by a function name, parentheses `()`, and a colon (`:`). The code that belongs to the function is indented.

```python
# Define a function named greet
def greet():
    print("Welcome to the world of functions.")
```

The code inside the function does not run until it is called. A **function call** is the expression that triggers the execution of a function by using its name followed by parentheses `()`.

```python
greet() # Output: Welcome to the world of functions.
```

---

## Passing Information to a Function: Parameters

A **parameter** is a variable listed inside a function's parentheses that acts as a placeholder for input values. The value provided when the function is called is known as an **argument**.

### Positional Arguments

A **positional argument** is an argument that is passed to a function in the correct positional order. The values are assigned to the function’s parameters based on their position in the function call.

```python
# 'system' and 'status' are parameters of this function
def report_status(system, status):
    print(system + " system is currently " + status + ".")

# 'Navigation' and ''Online are positional arguments
report_status("Navigation", "Online")
```

### Default Parameter

A **default parameter** is a function argument that has a predefined value. If no value is provided for that parameter when the function is called, the default value is used automatically.

```python
def initiate_docking(procedure="standard"):
    print("Initiating", procedure, "docking procedure.")

initiate_docking()            # Uses default
initiate_docking("emergency") # Overrides default
```

---

## Getting Information Back: The `return` Statement

The `return` statement sends a value back to the line of code that called the function.

```python
# This function takes a number, squares it, and returns the result
def square(number):
    result = number * number
    return result

# Call the function and store the returned value in a variable
squared_value = square(5)
print("The square of 5 is:", squared_value)

# You can also use the return value directly
print("The square of 10 is:", square(10))
```

---

## Documenting Your Functions: Docstrings

A **docstring** is a multi-line comment, enclosed in triple quotes (`"""`), placed at the beginning of a function definition to explain the its purpose.

```python
def function_name(param1, param2):
    """
    One-line summary of what the function does.

    More detailed description if necessary. Can include 
    behavior, side effects, and any notes about usage.

    Parameters:
        param1 (type): Description of the first parameter.
        param2 (type): Description of the second parameter.

    Returns:
        type: Description of the return value.

    Raises:
        ExceptionType: Description of why it might be raised.
    """
    # function logic here
```

### The `help()` Function

To access a function's docstring, use the built-in `help()` function.

Syntax: `help(object)`

```python
# Define a simple function with a docstring
def launch_sequence(destination: str, crew: int):
    """
    Initiates a simulated launch sequence.

    Parameters:
        destination (str): The name of the mission target (e.g., 'Mars').
        crew (int): Number of crew members onboard.

    Returns:
        None
    """
    print(f"Launching to {destination} with {crew} crew members.")

help(launch_sequence) # Info about the function's docstring
help(range)           # Info about the built-in range() function
help(str.upper)       # Info about a string method
help("for")           # Info about the "for" keyword
help()                # Enter interactive help (type 'quit' to exit)
```

---

## The `pass` Statement: A Placeholder

The `pass` statement is a placeholder that does nothing. It is used to define an empty function without causing an `IndentationError`.

```python
def check_fuel():
    # TODO: Add logic later
    pass

def check_crew():
    # This function is not implemented yet
    pass

# The program can call the function and it will do nothing 
check_fuel()
print("Program continues...")
```
