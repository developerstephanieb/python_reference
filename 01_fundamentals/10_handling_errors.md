# 10: Handling Errors

Programs crash and displays a traceback when it encounters a runtime error, such as a `NameError`. While tracebacks are great for developers, they are confusing for users.

A robust program should be able to anticipate and handle common errors gracefully without crashing. In Python, we do this using a `try...except` block.

---

## The `try...except` Block

The `try...except` block allows you to "try" to run a piece of code that might cause an error. If an error occurs, the code inside the `except` block is executed, and the program continues instead of crashing.

```python
try:
    # Code that might cause an error
    pass
except ErrorType:
    # Code to run if that specific error occurs
    pass
```

A common example is handling a `ValueError` when converting user input to a number. 

```python
# This program will crash if the user enters text like "ten"
age = int(input("Enter your age: "))
print("Your age is", age)
```

Now let's wrap it in a `try...except` block to handle the error gracefully.

```python
try:
    # Try to get and convert the user's input
    age = int(input("Enter your age: "))
    print("Next year, you will be", age + 1, "years old.")

except ValueError:
    # This block only runs if a ValueError occurs
    print("Invalid input. Please enter a number.")

print("The program continues without crashing.")
```

---

## Handling Multiple Specific Errors

A single `try` block can be followed by multiple `except` blocks to handle different types of errors in different ways.

```python
try:
    numerator = int(input("Enter the numerator: "))
    denominator = int(input("Enter the denominator: "))
    result = numerator / denominator
    print("The result is:", result)

# `ValueError` if the input isn't a number
except ValueError:
    print("Error: Both inputs must be numbers.")

# `ZeroDivisionError` if the user tries to divide by zero
except ZeroDivisionError:
    print("Error: Cannot divide by zero.")
```

---

## The `else` Block

Sometimes you have code that should only run if the `try` block was successful (i.e., no errors occurred). This code can be placed in an `else` block.

```python
try:
    number = int(input("Enter a number to divide 10 by: "))
    result = 10 / number

except ValueError:
    print("That was not a valid number.")

except ZeroDivisionError:
    print("You cannot divide by zero.")

else:
    # This code only runs if the try block completed without any errors
    print("The result of the division is:", result)
```

---

## The `finally` Block

There may be some code that you want to run no matter what, whether an error occurred or not. The `finally` block is always executed.

```python
try:
    number = int(input("Enter a number: "))
    result = 10 / number
    print("Result:", result)

except ValueError:
    print("Invalid input.")

finally:
    # This block will always run, regardless of whether an error happened
    print("--- End of attempt ---")
```
