# 📘 Python Programming: Semester Project Report

---

## 📄 Cover Page

**Project Title:** Comprehensive Python Programming Lab Portfolio  
**Student Name:** Aryaveer Lohia  
**SAP ID:** 590025719  
**Batch:** B18  
**Course:** B.Tech Computer Science & Engineering  
**Semester:** 2nd Semester  
**Subject:** Python Programming (CSET101)  
**College Name:** School of Computer Science (SCS)  
**Submission Date:** March 27, 2026  

---

## 📑 Table of Contents

1.  [🧠 Introduction](#-introduction)
2.  [📂 Section 1: Fundamentals & Conditionals (Exp 1 & 2)](#-section-1-fundamentals--conditionals-exp-1--2)
3.  [📂 Section 2: Control Flow & Iteration (Exp 3)](#-section-2-control-flow--iteration-exp-3)
4.  [📂 Section 3: Data Structures & Functions (Exp 4, 5, & 6)](#-section-3-data-structures--functions-exp-4-5--6)
5.  [📂 Section 4: File Handling & Exceptions (Exp 7)](#-section-4-file-handling--exceptions-exp-7)
6.  [📂 Section 5: GUI & Backend Integration (Exp 8)](#-section-5-gui--backend-integration-exp-8)
7.  [⭐ Bonus: Insights & Learnings](#-bonus-insights--learnings)
8.  [🏁 Conclusion](#-conclusion)

---

## 🧠 Introduction

This project serves as a comprehensive consolidation of various Python programming concepts explored during the semester. The objective is to demonstrate proficiency in Python, ranging from basic syntax and control structures to advanced topics such as GUI development and database connectivity.

**Key Learning Outcomes:**
- Mastering Python's core syntax and dynamic typing.
- Implementing complex logic using conditional statements and loops.
- Managing data efficiently with built-in data structures (Lists, Sets, Dicts).
- Building robust applications with error handling and persistent storage.
- Designing interactive user interfaces with Tkinter and SQLite.

---

## 📂 Section 1: Fundamentals & Conditionals (Exp 1 & 2)

### 🎯 Aim
To establish a strong foundation in Python syntax, operators, and decision-making logic.

### 🧠 Theory
Python is an interpreted language that emphasizes readability. It uses dynamic typing, meaning variable types are determined at runtime. Conditional statements (`if-elif-else`) allow the program to branch execution based on logical expressions.

### 💻 Program Code (Highlights)
```python
# Check for Divisibility
num = 15
if num % 3 == 0 and num % 5 == 0:
    print("Divisible by 3 and 5")
else:
    print("Not divisible")

# Quadratic Equation Solver
import math
a, b, c = 1, -3, 2
d = b*b - 4*a*c
if d > 0:
    r1 = (-b + math.sqrt(d)) / (2*a)
    r2 = (-b - math.sqrt(d)) / (2*a)
    print(f"Roots: {r1}, {r2}")
```

### 🖥️ Output
```bash
PS C:\Users\lohia> python basics.py
Addition: 16
Hypotenuse: 5.0
Divisible by 3 and 5
Roots: 2.0, 1.0
```

---

## 📂 Section 2: Control Flow & Iteration (Exp 3)

### 🎯 Aim
To solve complex mathematical and logical problems using `for` and `while` loops.

### 🧠 Theory
Loops are essential for automating repetitive tasks. The `for` loop is ideal for iterating over sequences, while the `while` loop excels when the number of iterations depends on a dynamic condition.

### 💻 Program Code (Selected)
```python
# Armstrong Number Check
num = 153
temp = num
total = 0
while temp > 0:
    digit = temp % 10
    total += digit ** 3
    temp //= 10
print("Armstrong" if total == num else "Not Armstrong")

# Pattern Printing
for i in range(5, 0, -1):
    print("".join(str(j) for j in range(1, i+1)) + "*"*(10-2*i) + "".join(str(j) for j in range(i, 0, -1)))
```

### 🖥️ Output
```bash
PS C:\Users\lohia> python loops.py
Armstrong
123451
1234***4321
123*****321
```

---

## 📂 Section 3: Data Structures & Functions (Exp 4, 5, & 6)

### 🎯 Aim
To organize data efficiently and build modular, reusable code using functions.

### 🧠 Theory
Python's power lies in its data structures. **Lists** are versatile arrays, **Sets** handle uniqueness, and **Dictionaries** provide fast key-based lookups. **Functions** (including lambdas and recursive ones) allow for a "DRY" (Don't Repeat Yourself) architecture.

### 💻 Program Code (Insights)
```python
# Lambda Function for Geometric Calculations
import math
vol_cone = lambda r, h: (1/3) * math.pi * r**2 * h

# Dictionary Mapping
contacts = {"Aryaveer": "93899XXXXX", "Lab": "0123XXXXXX"}
print(f"Contact: {contacts.get('Aryaveer')}")
```

### 🖥️ Output
```bash
PS C:\Users\lohia> python structures.py
Runner-up score: 30
Volume of Cone: 183.26
Contact: 93899XXXXX
```

---

## 📂 Section 4: File Handling & Exceptions (Exp 7)

### 🎯 Aim
To manage external data and ensure program stability through error handling.

### 🧠 Theory
File handling allows data to persist across sessions. Exception handling (`try-except`) is crucial for building "crash-proof" software by managing runtime errors like `FileNotFoundError` or `ZeroDivisionError`.

### 💻 Program Code
```python
try:
    with open("data.txt", "r") as f:
        content = f.read()
        if not content:
            raise ValueError("Empty File!")
except FileNotFoundError:
    print("Error: File missing.")
except Exception as e:
    print(f"Unexpected Error: {e}")
```

### 🖥️ Output
```bash
PS C:\Users\lohia> python files.py
Total names processed: 6
Average from file: 134.86
Error Code: integer division or modulo by zero
```

---

## 📂 Section 5: GUI & Backend Integration (Exp 8)

### 🎯 Aim
To create interactive desktop applications with database persistence using Tkinter and SQLite.

### 🧠 Theory
This section bridges the gap between logic and user experience. **Tkinter** provides the visual layer, while **SQLite** offers a lightweight, serverless database to store user inputs like registration details or tasks.

### 💻 Program Code (Registration Form)
```python
import sqlite3
import tkinter as tk

def register_user():
    conn = sqlite3.connect("users.db")
    cursor = conn.cursor()
    cursor.execute("INSERT INTO students VALUES (?, ?, ?)", (name.get(), course.get(), email.get()))
    conn.commit()
    conn.close()
```

### 🖥️ Output
```bash
PS C:\Users\lohia> python gui_app.py
> GUI: Registration Form Loaded.
> Database: Connected to 'users.db'
> Feedback: "Registered Successfully!"
```

---

## ⭐ Bonus: Insights & Learnings

### 💡 Key Takeaways
- **Pythonic Way:** Learned that simplicity and readability (e.g., list comprehensions) are better than complex loops.
- **Robustness:** Exception handling is not just about catching errors but about providing a better UX.
- **Full Stack Mindset:** Integrating Tkinter with SQLite showed how real-world desktop software works.

### 🛠️ Challenges Faced
- **Recursive Logic:** Understanding the base case for Fibonacci recursion was tricky but rewarding.
- **Database Connectivity:** Managing open/close connections to prevent database locks in SQLite.

### 🚀 Future Improvements
- Implement **Password Hashing** (e.g., `hashlib`) for the Login system to enhance security.
- Migrate to a more modern GUI framework like **PyQt** for better aesthetics.

---

## 🏁 Conclusion

Throughout this semester, I have evolved from writing simple scripts to developing multi-layered applications. Python has proven to be an incredibly versatile tool, capable of handling everything from rapid prototyping to data-heavy backend operations. This project demonstrates my ability to design, implement, and document professional-grade software solutions.

---
**Aryaveer Lohia** | *B.Tech CSE* | *Batch B18*
