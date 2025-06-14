---
created: 2025-06-14T14:55  
updated: 2025-06-14T14:55  
---

# Python List & Built-in Functions  
## Overview  
This lecture covers foundational knowledge about Python's `list` data structure, its built-in methods, and functions frequently used with lists. It also includes hands-on practices for list manipulation and a problem-solving section with classic problems like **Sum of Even Numbers** and **Two Sum**.

---

## 1. Introduction to Lists  

### Definition  
A list is a **mutable**, **ordered**, and **indexable** collection that can store elements of different data types (heterogeneous). Lists allow **duplicate values**.

```python
data = [4, 5, 6, 7, 8, 9]
```

### Features
- **Ordered and Duplicated**
- **Indexable**: Supports both forward and backward indexing.
- **Heterogeneous**: Can contain `int`, `float`, `str`, `bool`, etc.

### Indexing & Slicing  
```python
data[0]      # Access first element
data[-1]     # Access last element
data[2:4]    # Slice from index 2 to 3
data[::2]    # Step slicing
```

---

## 2. List Methods  

### Adding Elements  
- `append(value)` – Add to end  
- `insert(index, value)` – Insert at position  
- `extend(iterable)` – Extend with multiple elements

### Removing Elements  
- `remove(value)` – Removes first match  
- `pop(index)` – Removes and returns item at index  
- `clear()` – Empties the list  
- `del list[i:j]` – Deletes slice of elements

### Modifying Elements  
```python
data[1] = 4  # Update index 1
```

### Utility Methods  
- `index(value)` – Get first index of value  
- `count(value)` – Count occurrences  
- `reverse()` – Reverse list in place  
- `copy()` – Shallow copy  
- `sort()` / `sort(reverse=True)` – Sort ascending/descending

### Operators  
- `+` – Concatenate lists  
- `*` – Repeat lists

---

## 3. Built-in Functions for Lists  

| Function | Description |
|----------|-------------|
| `len(list)` | Number of elements |
| `min(list)` / `max(list)` | Smallest/largest item |
| `sum(list)` | Sum of elements |
| `zip(list1, list2)` | Pair elements |
| `reversed(list)` | Returns reversed iterator |
| `sorted(list)` | Returns sorted list |
| `enumerate(list)` | Returns index-element pairs |

---

## 4. Practice Problems  

### Sum of Even Numbers  

**Using `for` loop:**
```python
def even_sum(data):
    result = 0
    for value in data:
        if value % 2 == 0:
            result += value
    return result
```

**Using `while` loop:**
```python
def even_sum(data):
    index = 0
    result = 0
    while index < len(data):
        if data[index] % 2 == 0:
            result += data[index]
        index += 1
    return result
```

*Example Input*: `[6, 5, 7, 1, 9, 2]` → Output: `8`

---

### Two Sum Problem  

> Given a list `data` and a target number, find all pairs of indices where the elements add up to the target.

**Brute-force approach (double loop):**
```python
def two_sum(nums, target):
    n = len(nums)
    ans = []
    for i in range(n):
        for j in range(i+1, n):
            if nums[i] + nums[j] == target:
                ans.append([i, j])
    return ans
```

**Optimized using Hash Map:**
```python
def two_sum(data, target):
    num_indices = {}
    ans = []
    for i, num in enumerate(data):
        complement = target - num
        if complement in num_indices:
            ans.append([num_indices[complement], i])
        num_indices[num] = i
    return ans
```

*Example Input*: `[6, 5, 7, 1, 9, 2]`, `target = 8` → Output: `[[2, 3], [0, 5]]`

---

## 5. Summary  

### Key List Operations  
```python
# Create list
nums = [1, 2, 3]

# Index, slicing
nums[0]        # 1
nums[:2]       # [1, 2]

# Add/update/delete
nums.append(4)
nums[0] = 5
nums.pop(0)

# Utilities
nums.count(1)
nums.copy()
nums.sort()
```

### Built-in Functions  
- `len()`, `min()`, `max()`, `sum()`, `reversed()`, `enumerate()`, `zip()`

---

## Back Matter  
**Source**
- based_on: [[Week 2 Module 1]]

**References**
- 
**Task**
- Implement code examples and run variations  
- Complete practice problems: Even Sum & Two Sum  
- Try other built-in functions like `map()`, `filter()` for extension