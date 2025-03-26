# 🧠 Python Control Flow: Concepts Recap

## 🧩 What is Control Flow?
Control flow refers to the order in which individual statements, instructions, or function calls are executed or evaluated.

### Three Types of Control Flow:
1. **Sequence** – The default mode where code executes line-by-line in order.
2. **Branching** – Decision-making with conditions using `if`, `elif`, and `else`.
3. **Looping** – Repeating code while a condition is met, using loops like `for` and `while`.

---

## 🔁 Why it Matters:
- Control flow determines logic, decision-making, and behavior in all programs.
- These patterns are consistent across most programming languages (including JavaScript and Python).
- Once you understand control flow in one language, applying it to another becomes easier.

---

## ✅ Python Keywords for Control Flow
- **if** – Executes a block if the condition is true.
- **elif** – Else if; checks another condition if the first is false.
- **else** – Executes a block if no prior condition matched.
- **for** – Iterates over a sequence (like a list).
- **while** – Repeats as long as the condition is true.

---

## 🧠 Tip:
Learning your first programming language is the hardest. Each one after that gets easier because the core ideas like control flow stay the same!

---

## 🔍 Truthy and Falsy in Python

In Python, every piece of data is either **truthy** or **falsy**. This is important for control flow, especially in `if` statements and loops.

### Falsy Values:
- `False`
- `None`
- Zero values: `0`, `0.0`
- Empty sequences or collections:
  - `''` (empty string)
  - `[]` (empty list)
  - `()` (empty tuple)
  - `{}` (empty dictionary)
  - `range(0)` (empty range)

💡 **Note**: Unlike JavaScript, `[]` and `{}` are **falsy** in Python.

All other values are considered **truthy** by default.

---

## 🔣 Boolean Logic in Python

Boolean logic helps evaluate conditional expressions that determine how your code behaves.

### 🔢 Boolean Values
- Python has two boolean values: `True` and `False`.
- These are case-sensitive and must be capitalized.
  
### ⚖️ Equality Operators
- `==` – equal to (like `===` in JavaScript)
- `!=` – not equal

```python
print(7 == 7)       # True
print(7 == "7")     # False
print(7 != 7)       # False
print(7 != "7")     # True
```

### 📊 Comparison Operators
- `<` – less than
- `>` – greater than
- `<=` – less than or equal
- `>=` – greater than or equal

```python
print(8 > 8)        # False
print(8 >= 8)       # True
print(8 < 8)        # False
```

### 🔗 Logical Operators
Python uses plain English for logical operators:
- `or` – returns the first truthy operand, or the last one
- `and` – returns the first falsy operand, or the last one

```python
# or
print(True or False)       # True
print('hello' or 0)        # 'hello'
print(0 or 'hello')        # 'hello'
print('hello' or 'tacos')  # 'hello'

# and
print(True and False)      # False
print('hello' and 0)       # 0
print('hello' and 'tacos') # 'tacos'
```

### ⚠️ Mixing Logic
```python
print(False or True and True)  # True
```

Be cautious when mixing `and` and `or` as it can impact readability.

### 🚫 The `not` Operator
The `not` operator inverts a truthy/falsy value:

```python
print(not False)     # True
print(not 'hello')   # False
```

---

## 🌿 Branching with if, elif, else

Branching allows your code to take different paths based on conditions.

### 🔍 Basic if statement
```python
if condition:
    # code block executes if condition is True
```

### ✌️ if...else statement
```python
if condition:
    # do this
else:
    # do that
```

### 🔄 if...elif...else statement
```python
if condition1:
    # block 1
elif condition2:
    # block 2
else:
    # block 3
```

### 🧠 Python Syntax Rules
- No parentheses needed around conditions
- **Colons** (`:`) are required after the condition
- **Indentation** is mandatory (PEP8 recommends 4 spaces)

### 📌 Example
```python
val = 3

if val == 1:
    print("val is one")
elif val == 2:
    print("val is two")
elif val == 3:
    print("val is three")
else:
    print("not one, two, or three")
```

### 🎯 User Input Example
```python
color = input('Enter "green", "yellow", "red": ').lower()
print(f'The user entered {color}')

if color == "green":
    print("Go!")
elif color == "yellow":
    print("Slow Down!")
elif color == "red":
    print("Stop!")
else:
print("Bogus!")

---

## 🔁 Looping in Python

Looping lets you repeat blocks of code—perfect for when you want to iterate over items or run something multiple times.

### 🔂 `for` Loop

The `for` loop in Python iterates over sequences like lists, strings, or ranges.

```python
names = ["Emily", "Jack", "Sophia", "Ethan"]

for name in names:
    print(name)
```

💡 This is similar to JavaScript’s `for...of` loop.

---

### 🔁 `while` Loop

The `while` loop keeps executing as long as a condition is `True`.

```python
num = 1

while num <= 10:
    print(num)
    num += 1
```

⚠️ Make sure to include a condition that eventually becomes falsy to avoid infinite loops.

---

### 🛑 `break` and `continue`

- `break` exits the loop immediately.
- `continue` skips the rest of the loop and proceeds to the next iteration.

```python
things = ["computer", "g-g-ghost", "chair", "spider", "desk"]

for thing in things:
    if thing == "g-g-ghost":
        print("Oh, that's just my ghost friend, carry on.")
        continue
    elif thing == "spider":
        print("Nope. Burn it down, no more.")
        break
    print(f"There is a {thing} in the room.")
```

---

### 🎯 Looping with User Input

Wrap your previous input code inside a `while` loop so that the program keeps asking for input until `"quit"` is entered.

```python
while True:
    color = input('Enter "green", "yellow", "red" or "quit": ').lower()
    if color == "quit":
        break

    print(f'The user entered {color}')

    if color == "green":
        print("Go!")
    elif color == "yellow":
        print("Slow Down!")
    elif color == "red":
        print("Stop!")
    else:
        print("Bogus!")
```

🧠 This demonstrates dynamic input and looping combined!

---

## ⚡ Ternary Expressions in Python

Ternary expressions allow you to write simple conditional assignments in a single line.

### 💡 Syntax:
```python
value_if_true if condition else value_if_false
```

### ✅ Example:
```python
time_of_day = 9
morning = True if time_of_day < 12 else False
print(morning)  # prints: True
```

This is equivalent to:

```python
if time_of_day < 12:
    morning = True
else:
    morning = False
```

🧠 Use ternary expressions when you need quick inline conditionals.

---

## 📏 Working with `range()` in Python

The `range()` function in Python is commonly used in `for` loops to generate a sequence of numbers.

### 🔹 Basic Usage
```python
for num in range(5):
    print(num)
# Output: 0, 1, 2, 3, 4
```

- Starts at `0` by default.
- Ends before the specified number.
- Increments by `1` by default.

### 🔸 Start, Stop, Step
You can also pass in a starting point and a step:

```python
for even in range(4, 12, 2):
    print(even)
# Output: 4, 6, 8, 10
```

- `4` is the starting number.
- `12` is the stopping point (non-inclusive).
- `2` is the step (skip by 2s).

### 🔻 Negative Step
Count down using a negative step:

```python
for num in range(5, 0, -1):
    print(num)
# Output: 5, 4, 3, 2, 1
```

### 🔁 Create a List from a Range
Use `list()` to turn a range into a list:

```python
nums = list(range(10))
print(nums)
# Output: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

💡 `range` is memory efficient—it doesn't generate the entire list until needed, making it ideal for large sequences.

---

## 🎓 Control Flow Lab Summary

The Control Flow Lab applied your Python knowledge to real-world use cases. Here's a breakdown of the core skills and patterns practiced:

### ✅ Functions & Execution Flow
Each exercise was wrapped in a function using `def`, reinforcing structured, reusable code blocks.

### 🔣 User Input Handling
You practiced collecting and validating user input using `input()` and checking data with `.isalpha()`, `.isdigit()`, and `try/except` for type conversions.

### 🔄 Conditionals
All exercises used:
- `if/elif/else` logic
- Comparison operators (`==`, `!=`, `<`, `>=`)
- Boolean operators (`and`, `or`, `not`)

### 🧪 Defensive Programming
You learned to anticipate invalid user input and respond with clear feedback, e.g. checking for negative numbers or invalid types.

### 🐾 Logical Modeling
You implemented real-world logic like:
- Checking voting eligibility
- Determining dog years
- Giving weather advice based on multiple inputs
- Mapping seasons to month/day combinations
- Running a number guessing game with multiple attempts

### 🎯 Game Logic with Loops
The number guessing game used a `for` loop with `break`, demonstrating structured iteration with user input.

---

These exercises reinforce Python control flow fundamentals while building confidence in:
- Writing custom logic
- Validating input
- Handling conditions and loops gracefully

You're building habits that scale from command-line utilities to full-stack web apps. Keep going!