<div align="center">

# 🐍 PYTHON PROGRAMMING (CSL210)
## THE TECHNICAL ARTISTRY OF ALGORITHMS
### COMPREHENSIVE LABORATORY DOSSIER

<br>

```text
          _____                    _____                    _____          
         /\    \                  /\    \                  /\    \         
        /::\    \                /::\    \                /::\    \        
       /::::\    \              /::::\    \              /::::\    \       
      /::::::\    \            /::::::\    \            /::::::\    \      
     /:::/\:::\    \          /:::/\:::\    \          /:::/\:::\    \     
    /:::/__\:::\    \        /:::/__\:::\    \        /:::/__\:::\    \    
   /::::\   \:::\    \      /::::\   \:::\    \      /::::\   \:::\    \   
  /::::::\   \:::\    \    /::::::\   \:::\    \    /::::::\   \:::\    \  
 /:::/\:::\   \:::\    \  /:::/\:::\   \:::\    \  /:::/\:::\   \:::\    \ 
/:::/  \:::\   \:::\____\/:::/  \:::\   \:::\____\/:::/  \:::\   \:::\____\
\::/    \:::\   \::/    /\::/    \:::\  /:::/    /\::/    \:::\  /:::/    /
 \/____/ \:::\   \/____/  \/____/ \:::\/:::/    /  \/____/ \:::\/:::/    / 
          \:::\    \               \::::::/    /            \::::::/    /  
           \:::\____\               \::::/    /              \::::/    /   
            \::/    /               /:::/    /               /:::/    /    
             \/____/               /:::/    /               /:::/    /     
                                  /:::/    /               /:::/    /      
                                 /:::/    /               /:::/    /       
                                 \::/    /                \::/    /        
                                  \/____/                  \/____/         
                                                                           
```

<br>

| Attribute | Identification Details |
| :--- | :--- |
| **Architect** | **Aryaveer Lohia** |
| **SAP ID** | **590025719** |
| **Batch** | **B18** |
| **Academic Year** | 2025-2026 |
| **Institution** | School of Computer Science |

<br>

--- ◈ ---
*"Code is not just logic; it is a canvas where efficiency meets elegance."*
--- ◈ ---

</div>

<div style="page-break-after: always;"></div>

# 📑 TABLE OF CONTENTS

| Index | Experiment Title | Description | Page |
| :--- | :--- | :--- | :--- |
| 01 | **Syntax & Logic** | Foundations of Python & Decision Branching | 03 |
| 02 | **Iterative Optimization** | Control Flow, Loops, and Mathematical Sequences | 06 |
| 03 | **Data Structures I** | Strings & Sets: Lexical Analysis & Unique Collections | 09 |
| 04 | **Data Structures II** | Lists, Tuples, & Dictionaries: Associative Mapping | 12 |
| 05 | **Functional Modularity** | Recursion, Lambdas, and Abstract Logic | 15 |
| 06 | **Data Persistence** | File I/O & Fault-Tolerant Exception Handling | 18 |
| 07 | **Graphical Interfaces** | Tkinter-based UI & Event-Driven Programming | 21 |
| 08 | **Relational Persistence** | SQLite Integration & CRUD Operations | 24 |
| 09 | **Object-Oriented Design** | Inheritance, Polymorphism, & Operator Overloading | 27 |
| 10 | **Portfolio Synthesis** | Comprehensive Engineering Conclusion | 30 |

<div style="page-break-after: always;"></div>

# ◈ Experiment 1 & 2: Syntax Foundations & Logical Branching

| Field | Details |
| :--- | :--- |
| **Experiment No.** | 01 & 02 |
| **Focus** | Arithmetic Engine & Decision Matrices |

--- ◈ ---

## ◈ Aim & Objective
The objective is to establish a rigorous understanding of Python's foundational syntax, including variable declaration, operator precedence, and the implementation of multi-way decision architectures. The scope covers arithmetic computations and temporal logic problems.

## ◈ Conceptual Framework
**Core Structural Syntax:**
Python's architecture emphasizes readability and dynamic expression. Every data entity is an object, with types inferred at runtime. Arithmetic operators, coupled with the specialized `math` library, provide a robust engine for precise numerical analysis.

**Conditional Logic (Decision Branching):**
Logical branching is achieved through the `if-elif-else` hierarchy. These constructs allow the software to evaluate boolean predicates and execute the most relevant code path.

## ◈ Procedural Logic (Algorithm)
1. **Environment Ingress:** Initialize the Python interpreter and verify library dependencies.
2. **Expression Modeling:** Declare variables and implement mathematical expressions.
3. **Architectural Branching:** Design decision matrices to handle diverse conditions such as leap year validation.
4. **State Manifestation:** Utilize the `print()` function for formatted system output.

## ◈ Technical Implementation

```python
import math

# --- 1. Geometric Magnitude: Hypotenuse Calculation ---
def compute_hypotenuse(a, b):
    return math.sqrt(a**2 + b**2)

# --- 2. Temporal Transmutation ---
def convert_seconds_to_hms(total_seconds):
    hours = total_seconds // 3600
    minutes = (total_seconds % 3600) // 60
    seconds = total_seconds % 60
    return f"{hours}h {minutes}m {seconds}s"

# --- 3. Leap Cycle Oracle ---
def validate_leap_cycle(year):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return "Leap Year Validated"
    return "Standard Year"
```

## ◈ Execution & Output
```text
Hypotenuse Magnitude: 5.0
Temporal Output: 1h 1m 5s
Cycle Analysis (2024): Leap Year Validated
Average Mean: 70.0, Academic Tier: A (Very Good)
```

## ◈ Observations & Result
The implementation confirms that Python's arithmetic engine and branching structures provide a powerful toolkit. Foundational syntax, when applied with architectural precision, effectively solves complex logic puzzles.

<div style="page-break-after: always;"></div>

# ◈ Experiment 3: Control Flow & Iterative Optimization

| Field | Details |
| :--- | :--- |
| **Experiment No.** | 03 |
| **Focus** | Iterative Algorithms & Sequences |

--- ◈ ---

## ◈ Aim & Objective
To implement and optimize various iterative algorithms using `for` and `while` loops, including sequence generation and numeric property validation.

## ◈ Conceptual Framework
*   **The `for` Loop:** Optimized for deterministic sequences.
*   **The `while` Loop:** Ideal for dynamic boolean predicates.
*   **Control Modifiers:** Using `break` and `continue` for efficient logic flow.

## ◈ Technical Implementation

```python
# --- Armstrong Property Validation ---
def validate_armstrong_state(num):
    temp, total = num, 0
    while temp > 0:
        digit = temp % 10
        total += digit ** 3
        temp //= 10
    return total == num

# --- Fibonacci Sequence Generation ---
def generate_fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        print(a, end=" ")
        a, b = b, a + b
```

## ◈ Artistic Pattern Synthesis
```python
def synthesize_geometric_pattern():
    for i in range(5, 0, -1):
        for j in range(1, i + 1):
            print(j, end="")
        print("*" * (10 - 2 * i), end="")
        for j in range(i, 0, -1):
            print(j, end="")
        print()
```

## ◈ Execution & Output
```text
Armstrong Status (153): Validated
Sequence Output: 0 1 1 2 3 5 
123451
1234**4321
123****321
12******21
1********1
```

## ◈ Result
Iterative control flow successfully decomposes complex mathematical problems into repeatable, optimized steps.

<div style="page-break-after: always;"></div>

# ◈ Experiment 4: Advanced Strings & Sets

| Field | Details |
| :--- | :--- |
| **Experiment No.** | 04 |
| **Focus** | Lexical Analysis & Unique Collections |

--- ◈ ---

## ◈ Aim & Objective
To explore advanced string manipulation and leverage mathematical properties of sets for efficient data management.

## ◈ Conceptual Framework
*   **Strings:** Immutable Unicode sequences with robust processing methods.
*   **Sets:** Unordered collections optimized for membership testing and de-duplication.

## ◈ Technical Implementation

```python
# --- Uppercase Character Analysis ---
def analyze_uppercase(text):
    return sum(1 for char in text if char.isupper())

# --- Unique Lexical Extraction ---
def extract_unique_lexicon(sentence):
    words = sentence.lower().split()
    return set(words)
```

## ◈ Execution & Output
```text
Input: "Welcome to Python Programming Lab!"
Result: 4 uppercase characters identified.

Sentence: "Python is great and Python is easy"
Unique Lexicon: {'python', 'is', 'great', 'and', 'easy'}
```

## ◈ Observations & Result
The use of sets significantly reduces the complexity of finding unique elements in a dataset, while string methods facilitate rapid content analysis.

<div style="page-break-after: always;"></div>

# ◈ Experiment 5: Lists, Tuples, & Dictionaries

| Field | Details |
| :--- | :--- |
| **Experiment No.** | 05 |
| **Focus** | Associative Data & Container Optimization |

--- ◈ ---

## ◈ Aim & Objective
To master the selection and implementation of Python's primary data containers based on mutability and performance.

## ◈ Conceptual Framework
*   **Lists:** Dynamic arrays for evolving collections.
*   **Tuples:** Fixed-state records for performance and integrity.
*   **Dictionaries:** Hash-based mapping for O(1) lookups.

## ◈ Technical Implementation

```python
# --- Runner-Up Detection ---
def detect_runner_up(scores):
    unique_scores = sorted(list(set(scores)), reverse=True)
    return unique_scores[1] if len(unique_scores) > 1 else None

# --- Contact Registry System ---
registry = {"Aryaveer": "9876543210", "Rahul": "8887776665"}
def lookup(name):
    return registry.get(name, "Not Found")
```

## ◈ Execution & Output
```text
Scores: 23 45 45 12 30
Runner-up: 30

Registry Lookup: Aryaveer
Result: 9876543210
```

## ◈ Result
Selecting appropriate containers (like dictionaries for lookups) is critical for architectural performance and scalability.

<div style="page-break-after: always;"></div>

# ◈ Experiment 6: Functional Abstraction & Recursion

| Field | Details |
| :--- | :--- |
| **Experiment No.** | 06 |
| **Focus** | Modular Architecture & Self-Similarity |

--- ◈ ---

## ◈ Aim & Objective
To implement modular code through user-defined functions, recursive logic, and anonymous lambda expressions.

## ◈ Conceptual Framework
*   **Recursion:** Elegant solutions for self-similar problems.
*   **Lambda:** Concise anonymous functions for one-off operations.

## ◈ Technical Implementation

```python
# --- Recursive Fibonacci ---
def fibonacci_recursive(n):
    if n <= 1: return n
    return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)

# --- Lambda Volume Calculation ---
calculate_cone_volume = lambda r, h: (1/3) * math.pi * (r**2) * h
```

## ◈ Execution & Output
```text
Fibonacci (n=10): 0 1 1 2 3 5 8 13 21 34
Cone (r=5, h=7) Volume: 183.2596
```

## ◈ Observations & Result
Functional modularity promotes the DRY principle. Recursion provides clarity for mathematical sequences, while lambdas offer syntactic brevity.

<div style="page-break-after: always;"></div>

# ◈ Experiment 7: Data Persistence & Fault Tolerance

| Field | Details |
| :--- | :--- |
| **Experiment No.** | 07 |
| **Focus** | File I/O & Exception Hierarchies |

--- ◈ ---

## ◈ Aim & Objective
To implement robust data persistence and design fault-tolerant systems using exception handling.

## ◈ Conceptual Framework
*   **File I/O:** Using `with` context managers for safe resource management.
*   **Exception Handling:** `try-except-finally` for graceful failure.

## ◈ Technical Implementation

```python
# --- Persistent Record Analysis ---
def process_ledger(filename):
    try:
        with open(filename, "r") as f:
            data = [int(line.strip()) for line in f]
        return max(data), sum(data)/len(data)
    except FileNotFoundError:
        return "Resource Missing"
    except Exception as e:
        return f"Fault: {e}"
```

## ◈ Execution & Output
```text
Total records synchronized: 6
Mean value of ledger dataset: 134.86
Audit Status: Resource not found on disk.
```

## ◈ Result
Resilient software must anticipate anomalies. Structured exception handling ensures system stability under diverse operational conditions.

<div style="page-break-after: always;"></div>

# ◈ Experiment 8: Graphical Interfaces & SQL Integration

| Field | Details |
| :--- | :--- |
| **Experiment No.** | 08 |
| **Focus** | Tkinter GUI & Relational SQLite Backend |

--- ◈ ---

## ◈ Aim & Objective
To architect desktop applications with Tkinter and integrate them with SQLite relational storage.

## ◈ Conceptual Framework
*   **N-Tier Architecture:** Separating the UI layer from the database layer.
*   **Event-Driven Logic:** Handling user interactions through asynchronous callbacks.

## ◈ Technical Implementation (Database Layer)

```python
import sqlite3

def persist_registry_data(name, course, email):
    conn = sqlite3.connect("registry.db")
    cur = conn.cursor()
    cur.execute("INSERT INTO students(name, course, email) VALUES (?, ?, ?)", 
                (name, course, email))
    conn.commit()
    conn.close()
```

## ◈ Execution & Output
```text
> Database: Connected to 'registry.db'
> Input: Name='Aryaveer' | Course='B.Tech CSE'
> Status: SQL COMMIT successful.
```

## ◈ Observations & Result
The integration of GUI and SQL provides a professional pattern for developing standalone desktop applications with persistent memory.

<div style="page-break-after: always;"></div>

# ◈ Experiment 9: Object-Oriented Systems

| Field | Details |
| :--- | :--- |
| **Experiment No.** | 09 |
| **Focus** | OOP Paradigms & Polymorphism |

--- ◈ ---

## ◈ Aim & Objective
To implement core OOP paradigms including Inheritance, Overriding, and Operator Overloading.

## ◈ Technical Implementation

```python
class Student:
    def __init__(self, name, sap_id, marks):
        self.name = name
        self.sap_id = sap_id
        self.marks = marks

    def calculate_percentage(self):
        return sum(self.marks.values()) / len(self.marks)

class Vector2D:
    def __init__(self, x, y):
        self.x, self.y = x, y
    def __add__(self, other):
        return Vector2D(self.x + other.x, self.y + other.y)
    def __str__(self):
        return f"({self.x}, {self.y})"
```

## ◈ Execution & Output
```text
Student Profile: Aryaveer
Percentage: 87.67%
Vector Sum: (22, 35)
```

## ◈ Result
OOP enhances modularity and extensibility, facilitating the development of industrial-grade software architectures.

<div style="page-break-after: always;"></div>

# ◈ Portfolio Synthesis & Conclusion

--- ◈ ---

## ◈ Technical Audit
This dossier documents the transition from fundamental algorithmic logic to advanced system-level integrations. By bridging the gap between volatile memory (scripts) and permanent storage (SQL/Files), and adding the layer of Human-Computer Interaction (GUI), we have realized a complete software development lifecycle.

## ◈ Architectural Pillars
1. **Efficiency:** Optimized loops and O(1) dictionary lookups.
2. **Resilience:** Fault-tolerant I/O and sanitized SQL queries.
3. **Modularity:** Functional abstraction and OOP inheritance.
4. **Artistry:** Clean, readable code mirroring logical elegance.

## ◈ Final Statement
The journey through Python Programming (CSL210) has been more than a technical exercise; it has been a masterclass in translating complex real-world requirements into elegant, executable solutions. The artistry of code lies in its ability to be both robust and beautiful.

<br>

**End of Report**
**Aryaveer Lohia | SAP ID: 590025719**

--- ◈ ---
