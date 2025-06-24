---
created: 2025-06-24T21:06:00
updated: 2025-06-24T21:06:00
---
# 1. Introduction
- There are two way of coding: **Procedural programming** and **Object-oriented programming**
- While procedural programming focuses on functions and step-by-step instructions, object-oriented programming focuses on objects and the interactions between them.
![[Pasted image 20250624204557.png]]

- **OOP**: **Object-Oriented Programming (OOP)** aims to model software based on real-world entities. The main ide is to represent things like people, cars, books, or systems as objects in code, each having:
	- **Attributes (data)**: like name, color, size (these are represented as variables or fields).
	- **Behaviors (functions/methods)**: like move(), print(), calculate().
- **Class && Object**: Class && Object are core of OOP.
	- Class is a template of objects and an object is an instance of a class.
	![[Pasted image 20250624204937.png]]
	
# 2.Classes and Object In Python
- An attribute describes a characteristics of an object. For ex, a person has name, age, height...
- A method describes what an object can do. For ex, a person can write, read, walk...
- To define a class in Python:
![[Pasted image 20250624203424.png]]
![[Pasted image 20250624203524.png]]
- However, in OOP, we want to hide attributes, and allow them to be changed only through methods. Therefore, we put them in the private scope. We use `__var_name` to make an attribute private in Python.
![[Pasted image 20250624203908.png]]





# 3. Delegation
- **Motivation**: Delegation is a design technique where an object passes (or delegates) a task or behavior to another object, instead of doing it itself.
- Example:
A **Person** has a **name** (as a string) and a **date of birth**.  
A **Date** consists of **day**, **month**, and **year**.  
Instead of writing the date directly inside the `Person` class, we will create **`date_of_birth` as an instance of the `Date` class
![[Pasted image 20250624205436.png]]


# 4. Inheritance
- Definition: Mechanism by which one class is allowed to inherit the features (attributes and methods) of another class.
- Motivation: 
	1. Reuse Code: Inheritance allows child classes to reuse attributes and methods from a parent class, reducing code duplication.
	![[Pasted image 20250624210131.png]]
	2. Extensibility: Child classes can add new features or override existing ones without changing the parent class.
	For ex, a standard employee of company X includes his/her name and base salary. A manager includes his/her name, base salary, and bonus. The final salary for the manager comprises the Employee salary and a bonus.
	 ![[Pasted image 20250624210455.png]]
	 
	
	
	

# Back Matter

**Source**
- based_on: [[content/Module_1/Week_2/Week 2 Module 1]]
- 
**References**
- 