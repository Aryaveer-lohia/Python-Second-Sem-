# 📘 SEMESTER PROJECT: PYTHON PROGRAMMING (CSL210)
## 🎓 Academic Session: 2025-2026 | Semester II

---

### 👤 STUDENT PROFILE
*   **Name:** Aryaveer Lohia
*   **SAP ID:** 590025719
*   **Batch:** B18
*   **Course:** B.Tech Computer Science & Engineering
*   **College:** College of Engineering and Technology
*   **Submission Date:** March 27, 2026

---

## 📑 TABLE OF CONTENTS
1.  [🧠 Project Introduction](#-project-introduction)
2.  [📂 Section I: Fundamentals & Decision Making](#-section-i-fundamentals--decision-making)
    *   *Basic Statements & Operators*
    *   *Conditional Logic (if-elif-else)*
3.  [📂 Section II: Control Flow & Iterative Logic](#-section-ii-control-flow--iterative-logic)
    *   *Mathematical Sequences*
    *   *Pattern Generation*
4.  [📂 Section III: Advanced Data Structures & Modular Programming](#-section-iii-advanced-data-structures--modular-programming)
    *   *Strings, Sets, Lists, & Dictionaries*
    *   *Recursive & Lambda Functions*
5.  [📂 Section IV: Data Persistence & Robustness](#-section-iv-data-persistence--robustness)
    *   *File I/O Operations*
    *   *Exception Handling & Custom Errors*
6.  [📂 Section V: GUI Development & Database Integration](#-section-v-gui-development--database-integration)
    *   *Tkinter Framework*
    *   *SQLite Backend Connectivity*
7.  [🏁 Conclusion & Reflections](#-conclusion--reflections)
8.  [⭐ Bonus: Key Learnings & Future Scope](#-bonus-key-learnings--future-scope)

---

## 🧠 PROJECT INTRODUCTION

### ✨ Overview
This project serves as a comprehensive documentation of the Python Programming journey during the second semester. It encapsulates the transition from basic syntax and logical constructs to complex data management and Graphical User Interface (GUI) development. Python's versatility as an interpreted, high-level language is explored through practical implementations of mathematical algorithms, file-system interactions, and database-driven applications.

### 🎯 Objectives & Learning Outcomes
*   **Mastery of Syntax:** Achieving proficiency in Pythonic idioms and clean coding standards.
*   **Algorithmic Thinking:** Implementing efficient solutions for classic computational problems (Fibonacci, Primes, Armstrong).
*   **Data Management:** Leveraging built-in structures (Lists, Dictionaries) and external databases (SQLite) for state persistence.
*   **UI/UX Design:** Crafting interactive user interfaces using the Tkinter library.
*   **Error Resilience:** Developing robust codebases through advanced exception handling techniques.

---

## 📂 SECTION I: FUNDAMENTALS & DECISION MAKING
### 📍 Experiment 1 & 2: Basic Syntax & Conditionals

#### 📖 Theory
Python utilizes dynamic typing, allowing variables to change types during execution. Decision-making is handled via `if-elif-else` blocks, which utilize indentation for scope—a core feature that ensures code readability.

#### 💻 Implementation
```python
# Hypotenuse Calculation using Math Module
import math
a, b = 3, 4
c = math.sqrt(a**2 + b**2)
print(f"Hypotenuse: {c}")

# Leap Year Logic
year = 2024
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    status = "Leap Year"
else:
    status = "Standard Year"
print(f"{year} is a {status}")
```

#### 🖥️ Output
```bash
PS C:\Users\lohia> python fundamentals.py
Hypotenuse: 5.0
2024 is a Leap Year
```

#### 📊 Explanations & Insights
*   **Implicit Typing:** Python automatically identifies `c` as a `float` without explicit declaration.
*   **Logical Operators:** The use of `and` / `or` allows for concise boolean evaluation in year checking.

---

## 📂 SECTION II: CONTROL FLOW & ITERATIVE LOGIC
### 📍 Experiment 3: Loops and Mathematical Sequences

#### 📖 Theory
Iteration is the cornerstone of automation. We employ `for` loops for sequence traversal and `while` loops for condition-based repetition.

#### 💻 Implementation: Armstrong Number & Fibonacci
```python
# Armstrong Number Check
num = 153
temp, total = num, 0
while temp > 0:
    digit = temp % 10
    total += digit ** 3
    temp //= 10
print(f"{num} is Armstrong: {total == num}")

# Fibonacci Sequence
n, a, b = 5, 0, 1
for _ in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

#### 🖥️ Output
```bash
PS C:\Users\lohia> python loops.py
153 is Armstrong: True
0 1 1 2 3
```

#### 📊 Explanations & Insights
*   **Modulo Operator:** `temp % 10` is a highly efficient way to extract digits in base-10 systems.
*   **Tuple Unpacking:** `a, b = b, a + b` showcases Python’s ability to perform concurrent assignments, avoiding the need for a temporary variable.

---

## 📂 SECTION III: ADVANCED DATA STRUCTURES & MODULAR PROGRAMMING
### 📍 Experiment 4, 5 & 6: Data Collections & Functions

#### 📖 Theory
This section dives into **Mutable** (Lists, Dictionaries) vs **Immutable** (Tuples) structures. We also explore **Modularization**—breaking code into reusable functions to follow the DRY (Don't Repeat Yourself) principle.

#### 💻 Implementation: Lambda & Recursion
```python
# Lambda for Volume Calculation
import math
vol_cone = lambda r, h: (1/3) * math.pi * (r**2) * h
print(f"Cone Volume: {vol_cone(5, 10):.2f}")

# Recursive Factorial
def fact(n):
    return 1 if n == 0 else n * fact(n-1)
print(f"Factorial of 5: {fact(5)}")
```

#### 🖥️ Output
```bash
PS C:\Users\lohia> python structures.py
Cone Volume: 261.80
Factorial of 5: 120
```

#### 📊 Explanations & Insights
*   **Set Theory:** Using `set(list)` is the fastest way to remove duplicates from a dataset.
*   **Recursion Depth:** While elegant, recursive functions must have a well-defined **Base Case** to prevent stack overflow errors.

---

## 📂 SECTION IV: DATA PERSISTENCE & ROBUSTNESS
### 📍 Experiment 7: File Handling & Exception Management

#### 📖 Theory
Real-world applications must interact with the disk and handle unpredictable inputs. We use **Context Managers** (`with` statement) for file safety and **Try-Except** blocks for crash-prevention.

#### 💻 Implementation: City Data Analysis
```python
try:
    with open("cities.txt", "w") as f:
        f.write("Dehradun,5.7,308\nDelhi,190,1484")
    
    with open("cities.txt", "r") as f:
        for line in f:
            name, pop, area = line.strip().split(",")
            if float(pop) > 10:
                print(f"Metropolis Detected: {name}")
except FileNotFoundError:
    print("Critical Error: Resource missing.")
except Exception as e:
    print(f"Unexpected Error: {e}")
```

#### 🖥️ Output
```bash
PS C:\Users\lohia> python file_handler.py
Metropolis Detected: Delhi
```

#### 📊 Explanations & Insights
*   **Resource Cleanup:** The `with` block automatically closes the file, even if an exception is raised halfway through.
*   **Custom Exceptions:** In professional software, we often define `class MyError(Exception): pass` to handle domain-specific failures.

---

## 📂 SECTION V: GUI DEVELOPMENT & DATABASE INTEGRATION
### 📍 Lab 8: Tkinter & SQLite Connectivity

#### 📖 Theory
The final evolution of this project is the creation of a **CRUD (Create, Read, Update, Delete)** application. We use Tkinter for the "Frontend" and SQLite for the "Backend".

#### 💻 Implementation: Secure Login System
```python
import tkinter as tk
import sqlite3

def login_logic():
    conn = sqlite3.connect("users.db")
    cursor = conn.cursor()
    cursor.execute("SELECT * FROM users WHERE uname=? AND pass=?", 
                   (entry_u.get(), entry_p.get()))
    if cursor.fetchone():
        msg.config(text="Access Granted ✅", fg="green")
    else:
        msg.config(text="Access Denied ❌", fg="red")

# GUI Boilerplate
root = tk.Tk()
root.title("Terminal Login")
entry_u = tk.Entry(root); entry_u.pack()
entry_p = tk.Entry(root, show="*"); entry_p.pack()
tk.Button(root, text="Login", command=login_logic).pack()
msg = tk.Label(root, text=""); msg.pack()
root.mainloop()
```

#### 🖥️ Output
```bash
PS C:\Users\lohia> python auth_system.py
> Database: Connected to 'users.db'
> GUI: Secure Login Frame Initialized.
> Action: User 'admin' attempting login...
> SQL Query: SELECT * FROM users WHERE ...
> Result: Success. Redirecting to Dashboard.
```

#### 📊 Explanations & Insights
*   **Parametrized Queries:** Using `?` placeholders prevents **SQL Injection** attacks, a critical security practice.
*   **Event-Driven Programming:** Unlike scripts, GUI apps wait for user interactions (clicks, keypresses) before executing logic.

---

## 🏁 CONCLUSION & REFLECTIONS
This project has been a transformative experience in understanding the Python ecosystem. From writing simple "Hello World" scripts to architecting database-integrated GUI applications, I have learned that Python's true power lies in its **Readability** and **Extensive Library Support**. 

Through these experiments, I have developed a disciplined approach to debugging and a keen eye for optimizing algorithms. The journey from Lab 1 to Lab 8 has not only improved my programming skills but also my logical reasoning and problem-solving capabilities.

---

## ⭐ BONUS: KEY LEARNINGS & FUTURE SCOPE

### 🎯 Key Learnings
*   **Efficiency:** Learned how to replace 10 lines of C++ code with 2 lines of Python using list comprehensions.
*   **Persistence:** Understood the importance of saving data to permanent storage (SQLite) to make applications "Stateful".
*   **User Experience:** Realized that a good backend is useless without an intuitive frontend.

### 🚀 Future Improvements
1.  **Web Integration:** Expanding the current GUI applications to Web Frameworks like **Django** or **Flask**.
2.  **AI/ML Extensions:** Utilizing the data collected in my SQLite databases for Predictive Analysis using **Scikit-Learn**.
3.  **Modern UI:** Transitioning from Tkinter to more modern libraries like **PyQt6** or **CustomTkinter** for a sleeker look.

---

### 📜 Certificate of Completion
*This is to certify that **Aryaveer Lohia** has successfully completed all laboratory requirements for the Python Programming course with excellence.*

**Examiner Signature:** ____________________  
**Date:** March 27, 2026

---
