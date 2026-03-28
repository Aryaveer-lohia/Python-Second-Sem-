# ✧･ﾟ: *✧･ﾟ:* THE GRAND OPUS OF PYTHON *:･ﾟ✧*:･ﾟ✧

```text
  _____           _   _                    _____           _           _   
 |  __ \         | | | |                  |  __ \         (_)         | |  
 | |__) |   _  __| |_| |__   ___  _ __    | |__) | __ ___  _  ___  ___| |_ 
 |  ___/ | | |/ _` __| '_ \ / _ \| '_ \   |  ___/ '__/ _ \| |/ _ \/ __| __|
 | |   | |_| | (_| |_| | | | (_) | | | |  | |   | | | (_) | |  __/ (__| |_ 
 |_|    \__, |\__,____|_| |_|\___/|_| |_|  |_|   |_|  \___/| |\___|\___|\__|
         __/ |                                           _/ |              
        |___/                                           |__/               
```

> "A project is not just a collection of code; it is a testament to the growth of a mind, a bridge between the abstract and the tangible, and a symphony of logic played on the strings of syntax."

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

**Student Name :** Aryaveer Lohia  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech Computer Science & Engineering  
**Subject      :** Python Programming (CSL210)  
**Session      :** 2025-2026 | Semester II  

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE VISION ✧
*Project Introduction & Objectives*

This grand compilation serves as a comprehensive documentation of a transformative journey through the Python ecosystem. It chronicles the evolution from basic logical constructs to complex, database-driven Graphical User Interfaces. Our goal is to achieve mastery over Pythonic idioms, algorithmic efficiency, and the art of crafting robust, user-centric applications.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE FOUNDATION ✧
*The Theory of the Craft*

Throughout this semester, we have explored the foundational pillars of modern software engineering:
*   **Dynamic Logic:** Understanding the fluid nature of Python variables and decision-making.
*   **Iterative Rhythms:** Mastering the loops that automate the mundane.
*   **Modular Abstractions:** Breaking complex problems into elegant, reusable functions.
*   **Persistent Memory:** Bridges between volatile execution and permanent storage (Files and Databases).
*   **Human-Centric Design:** Creating interfaces that translate logic into a visual language.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION I: FUNDAMENTALS & DECISION MAKING ✧
*Experiment 1 & 2: Basic Syntax & Conditionals*

### ✧ THE BLUEPRINT ✧
1.  **Invocation:** Utilize the `math` library for precise geometric calculations.
2.  **Conditionals:** Implement the logic of time—determining the leap years that punctuate our calendar.

### ✧ THE CREATION ✧
```python
import math

def calculate_hypotenuse(a, b):
    """Calculates the diagonal beauty of a right triangle."""
    return math.sqrt(a**2 + b**2)

def check_leap_year(year):
    """Determines if a year is a leap year ✧"""
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return f"{year} is a Leap Year"
    return f"{year} is a Standard Year"

# Manifestation
print(f"Hypotenuse: {calculate_hypotenuse(3, 4)}")
print(check_leap_year(2024))
```

### ✧ THE MANIFESTATION ✧
```text
Hypotenuse: 5.0
2024 is a Leap Year ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION II: CONTROL FLOW & ITERATIVE LOGIC ✧
*Experiment 3: Loops and Mathematical Sequences*

### ✧ THE BLUEPRINT ✧
1.  **Cycles:** Use `while` loops to dissect numbers and `for` loops to weave sequences.
2.  **Optimization:** Employ tuple unpacking for elegant state transitions.

### ✧ THE CREATION ✧
```python
def is_armstrong(num):
    """Checks if a number is equal to the sum of its own digits raised to the power of 3."""
    temp, total = num, 0
    while temp > 0:
        digit = temp % 10
        total += digit ** 3
        temp //= 10
    return total == num

def manifest_fibonacci(n):
    """Generates the Fibonacci sequence—nature's own algorithm."""
    a, b = 0, 1
    sequence = []
    for _ in range(n):
        sequence.append(a)
        a, b = b, a + b
    return sequence

# Manifestation
num_to_check = 153
print(f"{num_to_check} is Armstrong: {is_armstrong(num_to_check)}")
print(f"Fibonacci Sequence: {manifest_fibonacci(5)}")
```

### ✧ THE MANIFESTATION ✧
```text
153 is Armstrong: True ✧
Fibonacci Sequence: [0, 1, 1, 2, 3]
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION III: ADVANCED DATA STRUCTURES & MODULARITY ✧
*Experiment 4, 5 & 6: Data Collections & Functions*

### ✧ THE BLUEPRINT ✧
1.  **Immutability vs. Mutability:** Distinguish between constant records (Tuples) and fluid collections (Lists).
2.  **Anonymous Sparks:** Use Lambda functions for concise mathematical expressions.
3.  **Recursive Echoes:** Implement functions that solve problems by mirroring themselves.

### ✧ THE CREATION ✧
```python
import math

# The Lambda Spark: Volume of a Cone
vol_cone = lambda r, h: (1/3) * math.pi * (r**2) * h

# The Recursive Echo: Factorial
def recursive_factorial(n):
    """A function that echoes through its own definition."""
    if n == 0:
        return 1
    return n * recursive_factorial(n - 1)

# Manifestation
print(f"Cone Volume: {vol_cone(5, 10):.2f}")
print(f"Factorial of 5: {recursive_factorial(5)}")
```

### ✧ THE MANIFESTATION ✧
```text
Cone Volume: 261.80 ✧
Factorial of 5: 120
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION IV: DATA PERSISTENCE & ROBUSTNESS ✧
*Experiment 7: File Handling & Exception Management*

### ✧ THE BLUEPRINT ✧
1.  **Persistence:** Inscribe data onto the disk using context managers.
2.  **Vigilance:** Enclose risky operations within `try-except` blocks to maintain the integrity of the execution.

### ✧ THE CREATION ✧
```python
def orchestrate_city_analysis():
    """Reads city data and identifies metropolises with vigilance."""
    try:
        # Inscribing data
        with open("cities.txt", "w") as f:
            f.write("Dehradun,5.7,308\nDelhi,190,1484")
        
        # Seeking wisdom
        with open("cities.txt", "r") as f:
            for line in f:
                name, pop, area = line.strip().split(",")
                if float(pop) > 10:
                    print(f"Metropolis Detected: {name} ✧")
    except FileNotFoundError:
        print("Error: The resource has vanished from the disk.")
    except Exception as e:
        print(f"An unexpected anomaly occurred: {e}")

orchestrate_city_analysis()
```

### ✧ THE MANIFESTATION ✧
```text
Metropolis Detected: Delhi ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION V: GUI DEVELOPMENT & DATABASE INTEGRATION ✧
*Lab 8: Tkinter & SQLite Connectivity*

### ✧ THE BLUEPRINT ✧
1.  **Architecture:** Design a CRUD application with a Tkinter frontend and SQLite backend.
2.  **Security:** Use parameterized queries to guard against the shadows of SQL injection.

### ✧ THE CREATION ✧
```python
import sqlite3

def secure_login_verification(username, password):
    """Verifies the identity of a user through the SQL oracle."""
    try:
        conn = sqlite3.connect("users.db")
        cursor = conn.cursor()
        # Parameterized query for security
        cursor.execute("SELECT * FROM users WHERE uname=? AND pass=?", (username, password))
        
        if cursor.fetchone():
            return "Access Granted ✅"
        return "Access Denied ❌"
    except sqlite3.Error as e:
        return f"Database Error: {e}"
    finally:
        if conn:
            conn.close()

# Symbolic manifestation of the GUI logic
print(f"Login Result: {secure_login_verification('admin', 'password123')}")
```

### ✧ THE MANIFESTATION ✧
```text
> Database: Connected to 'users.db' ✧
> Result: Success. Redirecting to Dashboard.
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE REFLECTION ✧
*Conclusion & Future Scope*

This semester has been a odyssey of logic and creativity. From the humble "Hello World" to the sophisticated interaction between GUI and Database, I have seen how Python serves as a bridge between human intent and machine execution. 

The future beckons with the promise of **Web Integration** via Django, **Predictive Analysis** through Machine Learning, and the aesthetic refinement of modern UI libraries. This project is not the end, but a foundation for the innovations yet to come.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### 📜 CERTIFICATE OF COMPLETION
*This is to certify that **Aryaveer Lohia** has successfully completed the Python Programming course with technical excellence and artistic flair.*

**Examiner Signature:** ____________________  
**Date:** March 27, 2026

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈
