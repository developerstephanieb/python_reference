# 09: Importing Modules

A **module** is a file containing Python code. The process of making that code available to your script is called **importing**.

This enables better organization of code and provides access to the tools included in **Python’s Standard Library**, which is a collection of modules included in every Python installation.

---

## The `import` Statement

The `import` statement makes the entire module available to your program.

To use a function or variable from the module, use dot notation by writing the module's name followed by a dot (`.`). 

### The `math` Module

The `math` module provides access to mathematical functions and constants commonly used in calculations.

```python
# Import the entire math module
import math

# To use a function from the module, you must prefix it with the module's name
# followed by a dot (.). This is called "dot notation".
square_root = math.sqrt(16)
print("The square root of 16 is:", square_root)

pi_value = math.pi # Modules can also contain variables (constants)
print("The value of Pi is:", pi_value)
```

By using the `module.function()` syntax, Python knows exactly where to find the `sqrt()` function, avoiding conflicts with functions defined elsewhere in the code.

---

## Importing Specific Functions with `from`

Sometimes, only one or two specific functions from a module are needed. The `from...import` syntax allows specific items to be imported directly into the program’s scope.

### The `random` Module

The `random` module provides functions for generating random values.

```python
# Import only the choice and randint functions from the random module
from random import choice, randint

# Now you can use these functions directly without the module prefix
fruits = ["apple", "banana", "cherry"]
random_fruit = choice(fruits)
print("Your random fruit is:", random_fruit)

random_number = randint(1, 10) # Get a random integer between 1 and 10
print("Your random number is:", random_number)
```

While convenient, this approach can lead to naming conflicts if a function with the same name has already been defined elsewhere in the code.

---

## Giving a Module an Alias with `as`

If a module has a long name, a shorter, more convenient alias can be assigned using the `as` keyword.

```python
# Import the math module and give it the alias 'm'
import math as m

# Now you can use the shorter alias as the prefix
square_root = m.sqrt(25)
print(square_root)

pi_value = m.pi
print(pi_value)
```

Imported functions can also be aliased using the `as` keyword.

```python
from random import randint as get_random_integer

random_number = get_random_integer(1, 100)
print(random_number)
```
