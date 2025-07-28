# 05: Control Flow

**Control flow statements** are programming constructs that determine the order in which code is executed. They enable decision-making, looping, and branching, allowing a program to change its normal top-to-bottom flow based on conditions or repeated actions.

---

## The `if` Statement: Making Decisions

The `if` statement runs a block of code only if a certain condition is `True`.

The structure requires a condition that evaluates to a boolean (`True` or `False`), followed by a colon (`:`) and an indented block of code.

```python
age = 20

# This block only runs if the condition (age >= 18) is True.
if age >= 18:
    print("You are old enough to vote.")
    print("Please register if you haven't already.")

print("This line runs no matter what.")
```

---

## The `else` Statement: Handling the Alternative

The `else` statement runs one block of code if a condition is true, and a different block if it's false.

```python
age = 16

if age >= 18:
    print("You are old enough to vote.")
else:
    # This block runs because the condition was False.
    print("You are not yet old enough to vote.")
```

---

## The `elif` Statement: Checking Multiple Conditions

The `elif` statement (short for "else if") chains multiple conditions together. Python checks them in order and runs the code for the first condition that is `True`.

```python
score = 85

if score >= 90:
    print("Your grade is an A.")
elif score >= 80:
    # This condition is checked because the first one was False.
    # It is True, so this block runs.
    print("Your grade is a B.")
elif score >= 70:
    print("Your grade is a C.")
else:
    # This only runs if none of the above conditions were True.
    print("Your grade is a D or F.")
```

---

## Loops: Repeating Actions

**Loops** are used to execute a block of code multiple times. There are two main types of loops in Python: `while` loops and `for` loops.

### The `while` Loop

A `while` loop repeats a block of code as long as a certain condition remains `True`. It's important to ensure that the condition will eventually become `False` to avoid an **infinite loop**.

```python
# Countdown using a while loop
countdown = 5

while countdown > 0:
    print("T-minus", countdown)
    # Decrease the number by 1 in each iteration
    countdown -= 1

print("Liftoff!")
```

### The `for` Loop

A `for` loop iterates over a sequence, such as a string or a list of items.

```python
# List of planets
planets = ["Mercury", "Venus", "Earth", "Mars"]

# The loop runs once for each item in the 'planets' list.
# In each iteration, the 'planet' variable holds the current item.
for planet in planets:
    print("Now orbiting", planet)
```

### Looping with `range()`

To loop a specific number of times, use the built-in `range()` function, which returns a sequence of numbers.

Syntax: `range(start, stop, step)`

| Parameter | Required? | Description                                                        | Default |
| :-------: | :-------: | ------------------------------------------------------------------ | :-----: |
|   start   |    No     | An integer specifying where the sequence begins                    |    0    |
|   stop    |    Yes    | An integer specifying where the sequence ends (exclusive)          |   --    |
|   step    |    No     | An integer specifying the increment (or decrement) between numbers |    1    |

```python
# range(5) generates numbers from 0 up to (but not including) 5
for number in range(5):
    print("Looping, iteration number:", number)
```

### Controlling Loop Behavior with `break` and `continue`

The `break` and `continue` statements allow finer control over loop execution.

- **The `break` Statement**
  
   The `break` statement immediately exits the loop. The program continues to execute at the first line after the loop. This is most often used to stop a loop when a specific condition is met.

   ```python
    # List of numbers
    numbers = [1, 5, 12, 7, 22, 30]

    for number in numbers:
        print("Checking", number)
        if number == 7:
            print("Found it!")
            # Exit the loop immediately
            break
   ```

- **The `continue` Statement**
  
   The `continue` statement ends the current iteration and jumps to the next one. This is useful for skipping certain items without breaking the entire loop.

   ```python
    # Print only the even numbers from 0 to 9
    for number in range(10):
        # If the number is odd, skip to the next iteration
        if number % 2 != 0:
            continue
        
        # This line only runs if the 'continue' was not triggered
        print(number)
   ```
