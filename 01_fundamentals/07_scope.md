# 07: Scope

**Scope** refers to the region of code where a variable is accessible. A variable is only available from inside its scope.

---

## LEGB rule

When a variable is used, Python searches for its definition in a specific order of scopes. This search order is known as the **LEGB rule** (Local, Enclosing, Global, Built-in).

| Scope         | Description                               |
| ------------- | ----------------------------------------- |
| **L**ocal     | The current function's scope              |
| **E**nclosing | The scope of any enclosing functions      |
| **G**lobal    | The top level scope of a script or module |
| **B**uilt-in  | The special scope for built-in names      |

---

## Local Scope

A variable created inside a function belongs to the **local scope** of that function. It can only be used within that function.

```python
def greet():
    # 'message' is in the local scope of the greet() function
    message = "Hello from inside the function!"
    print(message)

greet()           # This will work and print the message
# print(message)  # This would raise a NameError
```

---

## Enclosing Scope

The **enclosing scope** exists for nested functions. The inner function can access variables from the outer (enclosing) function's scope.

```python
def outer_function():
    greeting = "Hello" # 'greeting' is in the enclosing scope for inner_function

    def inner_function():
        # 'inner_function' can access 'greeting' from its enclosing scope
        print(greeting + ", World!")

    inner_function()

outer_function() # Output: Hello, World!
```

---

## Global Scope

A variable defined in the main body of a Python script is in the **global scope**. It's accessible from any scope, global or local.

```python
# 'player_name' is a global variable
player_name = "Alex"

def print_player_name():
    # We can access the global 'player_name' variable from here
    print("Current player:", player_name)

print_player_name() # Output: The player's name is Alex
```

---

## Built-in Scope

The **built-in scope** contains all of Python’s predefined names, including functions like `print()` and `type()`. These are accessible throughout the program.

```python
# 'type' is a built-in function, so it's always available
animal = "dog"
print(type(animal)) # Output: <class 'str'>
```

---

## Modifying Variables Across Scopes

By default, you can only read variables from an outer scope. If you try to assign a new value, Python will create a new local variable with the same name instead. To explicitly modify a variable in an outer scope, use the `global` or `nonlocal` keywords.

### The `global` Keyword

To modify a variable in the global scope from inside a function, declare it with the `global` keyword.

```python
score = 100  # Global variable

def increase_score():
    # Use the 'global' keyword to modify the global variable
    global score
    score += 10
    print(f"Score inside function: {score}")

increase_score()                          # Output: Score inside function: 110
print(f"Score outside function: {score}") # Output: Score outside function: 110
```

### The `nonlocal` Keyword

To modify a variable in the enclosing scope from an inner function, use the `nonlocal` keyword.

```python
def game():
    level = "Easy" # Enclosing scope variable

    def start_level():
        nonlocal level
        level = "Hard" # Modifies the 'level' variable from the 'game' function

    start_level()
    print(f"Current level: {level}") # The change is reflected here

game() # Output: Current level: Hard
```

### Scope and Mutable Objects

To modify the contents of a mutable object (such as a list) inside a function, `global` and `nonlocal` are not required.

These keywords are only necessary when reassigning the entire variable to a new object within the function.

- Modifying a global list (OK without `global`):

    ```python
    items = ["sword"] # Global list

    def add_item(item):
        # This MODIFIES the existing global list, it doesn't reassign it.
        items.append(item)

    add_item("shield")
    print(items) # Output: ['sword', 'shield']
    ```

- Reassigning a global list (Needs `global`):

    ```python
    items = ["paper", "pen"] # Global list

    def replace_items():
        global items
        # This REASSIGNS the variable to a new list object.
        items = ["coin", "key"]

    replace_items()
    print(items) # Output: ['coin', 'key']
    ```
