# Introduction
In programming, we often need to repeat certain actions multiple times — for example, printing 10 similar lines. To handle these repetitive tasks efficiently, we use loops.
Python supports two main types of loops:
- `for loop` – used to iterate over a sequence (like a list, range, tuple, etc.)
- `while loop` – repeats as long as a condition is true
# FOR Loop
The `for` loop is used to iterate over each element in a list, string, tuple, dictionary, or any iterable object.
![[{CB76E023-E52B-48A8-8BF9-8AD9B94EBC46}.png]]

Breakdown of components:

- Keyword: Marks the start of the `for` loop. It tells Python you want to iterate over something.
- Colon: Indicates the end of the loop header and the beginning of the loop body.
- Indentation: Python uses indentation (usually 4 spaces or 1 tab) to define the block of code inside the loop
- element: A variable that represents each element from the `iterable`. On each iteration, it takes the next value.
- `iterable` : Any iterable object (like a list, string, tuple, or range) that provides the elements for the loop.

The `break` statement is used to **terminate the loop prematurely** when a specific condition is met. The `continue` statement is used to **skip the rest of the code inside the loop for the current iteration** and **jump to the next iteration**.
## Examples
```python
# Example 1: Loop through a string
word = "Python"
for i in word:
    print(i)
    
# Output:
# P
# y
# t
# h
# o
# n


# Example 2: Loop through a list
fruits = ["Apple", "Orange", "Banana"]
for fruit in fruits:
    print(fruit)
    
# Output:
# Apple
# Orange
# Banana


# Example 3: Loop through a sequence of numbers using range(begin, end, step)
# Explanation:
# - begin: starting number (inclusive)
# - end: ending number (exclusive)
# - step: step size between numbers (default is 1)

for i in range(2, 10, 2):
    print(i)
# Output:
# 2
# 4
# 6
# 8

```
- When you call `range(stop)`, passing **only one argument**:
    - `stop` is the ending value (exclusive).
    - The default **begin** is `0`.
    - The default **step** is `1`.
- When you call `range(start, stop)`, passing **two arguments**:
    - `start` is the starting value (inclusive).
    - `stop` is the ending value (exclusive).
    - The default **step** is still `1`.
- When you call `range(start, stop, step)`, passing **three arguments**:
    - `start` is the starting value.
    - `stop` is the ending value.
    - `step` is the step size (can be positive or negative).

```python
# Only one argument: range(stop)
print("range(5):")
for i in range(5):
    print(i)

# Output:
# 0
# 1
# 2
# 3
# 4


# Two arguments: range(start, stop)
print("\nrange(2, 6):")
for i in range(2, 6):
    print(i)

# Output:
# 2
# 3
# 4
# 5


# Three arguments: range(start, stop, step)
print("\nrange(1, 10, 3):")
for i in range(1, 10, 3):
    print(i)

# Output:
# 1
# 4
# 7


# Negative step example: counting backwards
print("\nrange(10, 0, -2):")
for i in range(10, 0, -2):
    print(i)

# Output:
# 10
# 8
# 6
# 4
# 2
```
Using break and continue in the loop
```python
print("Example with break:")
for i in range(1, 10):
    if i == 5:
        break
    print(i)

# Output:
# Example with break:
# 1
# 2
# 3
# 4

print("\nExample with continue:")
for i in range(1, 6):
    if i == 3:
        continue
    print(i)

# Output:
# Example with continue:
# 1
# 2
# 4
# 5
```
# WHILE Loop

![[{D3BE1F87-BB52-4EFD-A197-E0C3D8598114}.png]]
Breakdown of components:

- **Keyword (`while`)**:
    
    Marks the beginning of the loop. It tells Python to repeatedly execute the loop body **as long as the condition is `True`**.
    
- **Condition**:
    
    A boolean expression that is evaluated **before each iteration**.
    
    If the condition is `True`, the loop continues; if `False`, the loop stops.
    
- **Colon (`:`)**:
    
    Indicates the end of the loop header and the start of the loop body.
    
    It’s required to define the structure of the loop.
    
- **Indentation**:
    
    Defines the block of code that belongs to the loop body.
    
    Python uses indentation (usually 4 spaces) to determine which statements are inside the loop.
    

The `break` statement is used to **terminate the loop prematurely** when a specific condition is met. The `continue` statement is used to **skip the rest of the code inside the loop for the current iteration** and **jump to the next iteration**.
## Examples
```PYTHON
i = 0
while i < 5:  # Loop continues while i < 5
    print("i =", i)
    i += 1    # When i becomes 5, the condition is False and the loop stops

# Output:
# i = 0
# i = 1
# i = 2
# i = 3
# i = 4

#Using break to exit the loop
i = 0
while True:  # Infinite loop
    print("i =", i)
    if i == 3:
        break  # Breaks the loop when i == 3
    i += 1

# Output:
# i = 0
# i = 1
# i = 2
# i = 3
#Using continue to skip an iteration
i = 0
while i < 5:
    i += 1
    if i == 3:
        continue  # Skips the rest of the loop when i == 3
    print("i =", i)

# Output:
# i = 1
# i = 2
# i = 4
# i = 5

```
# When to Use for vs. while
|Situation|Use This Loop|
|---|---|
|You know how many times to loop / have a sequence|`for`|
|You want to loop until a condition is met|`while`|
# Back Matter

**Source**
- based_on: [[Module 1]]

**References**
- 