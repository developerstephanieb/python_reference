# 09: Importing Modules

A **module** is a file that contains Python code. Making the code from a module available to a script is called **importing**.

Importing allows for better code organization and provides access to tools from **Python’s Standard Library** - a collection of modules included with every Python installation.

---

## The `import` Statement

The `import` statement makes an entire module available to a program, allowing access to its functions, classes, and variables.

Syntax: `import module_name`

To access functions or variables from a module, use the dot notation: `module_name.item_name`. Including the full module name prevents conflicts with similar names defined elsewhere in the code.

### The `math` Module

The `math` module provides access to mathematical functions and constants commonly used in calculations.

```python
# Import the entire math module
import math

# Use a function from the module with dot notation
square_root = math.sqrt(16)
print("The square root of 16 is:", square_root)

pi_value = math.pi # Modules can also contain constants
print("The value of Pi is:", pi_value)
```

---

## Importing Specific Functions with `from`

Sometimes only specific functions or variables from a module are needed. The `from` keyword allows for selected items to be imported directly into the program’s scope, so they can be used without module prefixing.

Syntax: `from module_name import item1, item2, ...`

While convenient, this approach can lead to naming conflicts if a function with the same name has already been defined elsewhere in the code.

### The `random` Module

The `random` module provides functions for generating random values.

```python
# Import only the choice and randint functions from the random module
from random import choice, randint

# Now use these functions directly without the module prefix
fruits = ["apple", "banana", "cherry"]
random_fruit = choice(fruits)
print("Your random fruit is:", random_fruit)

random_number = randint(1, 10) # Get a random integer between 1 and 10
print("Your random number is:", random_number)
```

---

## Giving a Module an Alias with `as`

If a module has a long name, a shorter, more convenient alias can be assigned using the `as` keyword.

Syntax: `import module_name as alias`

```python
# Import the math module and give it the alias 'm'
import math as m

# Now use the shorter alias as the prefix
square_root = m.sqrt(25)
print(square_root)

pi_value = m.pi
print(pi_value)
```

Imported functions can also be aliased using the `as` keyword.

Syntax: `from module_name import item as alias`

```python
# Import only the randint function from random and give it the alias `get_random_integer`
from random import randint as get_random_integer

# Use the alias to generate a random integer between 1 and 100
random_number = get_random_integer(1, 100)
print(random_number)
```
