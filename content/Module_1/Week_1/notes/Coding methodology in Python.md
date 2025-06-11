---
created: 2025-06-10T17:33
updated: 2025-06-10T17:33
---
# Coding methodology in Python
## Clean Code
### Clean code definition
Clean code is source code which is **readable**, **maintainable, extensible and testable**. Clean code is written in the way that helps other people or even yourself in the future can easily understand, improve or maintain it.
![[Pasted image 20250609151243.png]]
### Core Principles of Clean Code (3D1C)
- **Readable (Dễ đọc, dễ hiểu)**: Code should be written so that others can easily understand its purpose and how it works
- **Maintainable (Dễ bảo trì)**: Clean code should be easy to modify, extend and reuse without causing new bugs
- **Testable (Dễ kiểm thử)**: Clean code should be designed to easily write unit test and automation test.
- **Extensible (Có khả năng mở rộng)**: Code should be designed to easily add new features without having to modify existing code
### Importance of Clean Code 
### When should you skip Clean Code
## PEP-8
PEP-8 (Python Enhancement Proposal 8) is the official Python coding conventions, created by Guido van Rossum, which created Python. Follow PEP-8 will help you write clean Python code.
### Naming convention
1. **Variable/Function: snake_case** (Use normal case and underscore to separate words)
2. **Class: PascalCase** (Capitalize the first letter of each word, No underscores)
3. **Constant: UPPER_CASE** (Capital all letters and use underscore)
### Indentation and spaces
- **Indent**: Uses 4 spaces (no tabs) 
- **Line length**: Up to 79 characters for code, 72 for docstring 
- **Whitespace**: Do not set in parentheses, only after the comma 
- **Mathematical Operations**: Put white space on both sides (x = 1)
### Import order
1. Python core libraries like: os, sys, math, ...
2. Third-party libraries (installed by pip): pandas, numpy, ...
3. Internal module (written in your code)
### Class/Function structure
- Class order: docstring -> class variables -> init function -> public methods -> private method (prefix with double underscores) -> static methods
- Function order: docstring -> validate arguments -> main code -> return
### White line
- Two white lines to separate between classes
- One white line to separate methods in a class
- One white lien to separate different logic in a function/method
### Code Documentation
Code documentation helps reduce the time spent reading to understand code, easier maintainance and collaboration.

- **Docstring**: follow popular styles:
	- **Google style**: concise, easy to read, used for general purpose code![[Pasted image 20250609151311.png]]
	- **Numpy style**: more detailed, ideal for scientific and mathematical projects![[Pasted image 20250609151332.png]]
- **Annotation and type hints**
	- Kiểu cơ bản: def add(a: int, b: float) -> float:
	- Kiểu phức tạp: from typing import List, Dict, Tuple, Optional
	- Kiểu Union: def process(data: Union[str, bytes]) -> None:
- **Project and module**
	- Module docstring: Put at the top of the file, description Purpose and main functions 
	- README.md: Installation instructions, e.g. Simple, Project Structure 
	- CONTRIBUTING.md: Closing process contributions, code rules 
	- Sphinx: Automatically generate API documentation from Docstring 
	- Wiki: Detailed documentation for features intricate
### Popular Python code linters
- **Pylint**: A comprehensive static code analysis tool that checks for a wide range of programming errors, enforces coding standards (like PEP 8), and identifies code smells, offering suggestions for refactoring.
- **Flake8**: A simpler and faster linter that acts as a wrapper, combining pycodestyle (for PEP 8 style adherence), PyFlakes (for basic syntax and logical errors), and McCabe (for checking code complexity).
- **Black**: An uncompromising and opinionated code formatter that automatically reformats Python code to a consistent style, aiming to eliminate style debates during code reviews.
- **isort**: A utility that automatically sorts Python imports alphabetically and separates them into logical sections, promoting clean and organized import statements.
- **Mypy**: A static type checker that helps enforce type hints (PEP 484) in Python code, catching type-related errors before runtime and improving code maintainability.
- **Ruff**: An extremely fast Python linter and code formatter written in Rust, designed to be a highly performant replacement for many existing tools like Flake8, isort, and others.
### Python project template
A well-organized Python project will be easy to maintain and scale. Below is the standard folder structure:
- Root Directory (project_name/): contains README, requirements.txt, setup.py
- Source code (project_name/src/): contains main modules and packages 
- Tests (project_name/tests/): contains test suites (unittest, pytest)
- Documentation (project_name/docs/): user Manual and API Documentation 
- Resources (project_name/resources/): static data, templates, assets 
- Use configuration files such as.gitignore, pyproject.toml, and README.md files to ensure project management is efficient and easy easy for others to understand and contribute.
https://github.com/khoanta-ai/python_project_template
https://github.com/drivendataorg/cookiecutter-data-science
## Pythonic Code
### The Zen of Python
A collection of 19 rules for writing Pythonic code by Tim Peters in PEP-20 (run "import this" in python):
The Zen of Python, by Tim Peters
- Beautiful is better than ugly.
- Explicit is better than implicit.
- Simple is better than complex.
- Complex is better than complicated.
- Flat is better than nested.
- Sparse is better than dense.
- Readability counts.
- Special cases aren't special enough to break the rules.
- Although practicality beats purity.
- Errors should never pass silently.
- Unless explicitly silenced.
- In the face of ambiguity, refuse the temptation to guess.
- There should be one-- and preferably only one --obvious way to do it.
- Although that way may not be obvious at first unless you're Dutch.
- Now is better than never.
- Although never is often better than *right* now.
- If the implementation is hard to explain, it's a bad idea.
- If the implementation is easy to explain, it may be a good idea.
- Namespaces are one honking great idea -- let's do more of those!
### Pythonic code examples
Pythonic means making the most of Python's unique features and characteristics to write code. Pythonic code is easy to read, easy to understand, faster, as concise as English reading, and adheres to Python conventions and philosophies
- List, Dict, Set comprehension![[Pasted image 20250610135840.png]]
- Context Manager: Context Manager is a resource management mechanism through the with statement, which automatically frees up resources (closing files, closing DB connections, freeing locks...) when the code block ends, even if an error occurs.![[Pasted image 20250610135859.png]]
- Properties and underscore in class:
	- @property: allow to use class method as an attribute, make code cleaner and easier to access.
	- Single underscore (\_var): private class attribute. Still can access from outside the class, but this is the sign about: "not using this directly"
	- Double underscore on left and right: magic/dunder method (init)
	- Double underscore: name mangling
## General Principles for Writing Good Code
### DRY (Don't Repeat Yourself)
- Write your code so that you don't have the same information or instructions in multiple spaces. If you need to change something, you only change it once.
### YAGNI (You Aren't Gonna Need It)
- You should only build things when you actually need them, not because you think you might need them in the future. It help keeps code simple and avoid wasted effort.
### KISS (Keep It Simple, Stupid)
- You should always try to make your code as simple, straightforward as possible, even if the problem is complex. Simpler
### Defensive programming
- Writing your code with the mindset to expect and handle things that could go wrong, like bad user input or unexpected situations. It's like building safety net to prevent your program to failed or acting weirdly.
### Separation of concerns
- Dividing your code into different parts (module, class, function) where each part handles a separate job of concern. This make your codes easier to manage, understand and change because you can focus on one part without messing up others.
### Print and Logging

| **Print**                           | **Logging**                                        |
| ----------------------------------- | -------------------------------------------------- |
| Simple, easy to use                 | Flexible configuration                             |
| Hard to control output              | Multiple log levels (DEBUG, INFO, WARNING...)      |
| No severity levels                  | Easy to enable/disable, according to configuration |
| Hard to turn off when deployed      | Automatically add time, file, line of code         |
| Does not save information like time | Can direct logs to file, email...                  |
![[Pasted image 20250610114010.png]]
## SOLID & Design Patterns

---
#   Back Matter

**Source**
- based_on: [[Week 1 Module 1]]

**References**
- 
**Task**
- Review code examples
- Do the exercises in the slide