---
created: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %> 
updated: <% tp.date.now("YYYY-MM-DDTHH:mm:ss") %>
---
# 1D List
- **Definition**: A list is a data structure used to store multiple elements.
- **Index:** Each element in a list can be accessed using an index, starting from 0. There are two types of indexing methods: **forward indexing**, which begins from the start of the list, and **backward indexing**, which starts from the end of the list
![[Pasted image 20250615221050.png]]
- Slice: Slicing allows you to extract specific elements from a list.![[Pasted image 20250615221446.png]]
- **Add an element:**
    - list.append(value): add an element to the end of the list
    ![[Pasted image 20250615221616.png]]

- list.insert(index, value): add an element to the index position of the list
![[Pasted image 20250615221905.png]]
- **Add a list of elements**: list.extend(a list)
![[Pasted image 20250615221937.png]]
- **Others:**
    - sort(): used to sort elements in a list (ascending order)
    - pop(index): used to delete an element at the specified index in a list
    - remove(value): delete the first element equal to value in a list
    - reverse(): used to reverse the order of elements in a list in place
- **Some built-in functions:**
    - len(): return the length of a list
    - min(): returns the smallest element in a list
    - max(): returns the largest element in a list
    - sorted(): used to sort elements in a list (ascending order)
    - sum(): used to calculate the sum of elements in a list
    - zip(): pairs elements from multiple iterables based on their positions![[Pasted image 20250615222121.png]]
    - enumerate(): adds a counter to an iterable and returns it as an enumerate object
    ![[Pasted image 20250615222207.png]]
    
- **List comprehension**: A list comprehension is a compact way to build a new list from another one![[Pasted image 20250615222336.png]]
# 2D List
- **Definition:** A 2D list is used to represent table-like data, matrices, or grids, which are common in: Math matrices (for calculations), Digital images (as pixel matrices)….
- A 2D list is considered a list that contains 1D lists as its elements
![[Pasted image 20250615222641.png]]
- **Hadamard Product (Element -wise Multiplication):** the element-by-element multiplication of two matrices (or 2D lists) of the same size.
![[Pasted image 20250615222705.png]]
---
# Back Matter

**Source**
- based_on: [[Week 2 Module 1]]
- 
**References**
- 