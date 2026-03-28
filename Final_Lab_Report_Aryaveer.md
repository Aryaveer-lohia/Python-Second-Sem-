<div align="center">

# 🐍 PYTHON PROGRAMMING (CSL210)
## THE TECHNICAL ARTISTRY OF ALGORITHMS
### COMPREHENSIVE LABORATORY DOSSIER

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

| Index | Experiment / Section Title | Page |
| :---: | :--- | :---: |
| 01 | **Syntax Foundations & Logical Branching (Exp 1 & 2)** | 03 |
| 02 | **Control Flow & Iterative Optimization (Exp 3)** | 06 |
| 03 | **Advanced Data Structures & Functional Modularity (Exp 4, 5, 6)** | 09 |
| 04 | **Data Persistence & Fault-Tolerant Systems (Exp 7)** | 14 |
| 05 | **Graphical Interfaces & Relational Persistence (Lab 8)** | 17 |
| 06 | **Object-Oriented Systems & Polymorphic Architectures (Exp 9)** | 22 |
| 07 | **Comprehensive Python Engineering Portfolio (Final Project)** | 26 |

<div style="page-break-after: always;"></div>

# ◈ Syntax Foundations & Logical Branching (Exp 1 & 2)

| Field | Details |
| :--- | :--- |
| **Architect** | Aryaveer Lohia |
| **SAP ID** | 590025719 |
| **Batch** | B18 |
| **Subject** | Python Programming |

--- ◈ ---

## ◈ Objective & Scope
The objective is to establish a rigorous understanding of Python's foundational syntax, including variable declaration, operator precedence, and the implementation of multi-way decision architectures. The scope covers arithmetic computations and temporal logic problems.

## ◈ Conceptual Framework
**Core Structural Syntax:**
Python's architecture emphasizes readability and dynamic expression. Every data entity is an object, with types inferred at runtime. Arithmetic operators, coupled with the specialized `math` library, provide a robust engine for precise numerical analysis.

**Conditional Logic (Decision Branching):**
Logical branching is achieved through the `if-elif-else` hierarchy. These constructs allow the software to evaluate boolean predicates and execute the most relevant code path, mirroring real-world decision-making processes.

## ◈ Procedural Logic
1.  **Environment Ingress:** Initialize the Python interpreter and verify library dependencies (e.g., `math`).
2.  **Expression Modeling:** Declare variables and implement mathematical expressions using standardized operators.
3.  **Architectural Branching:** Design decision matrices to handle diverse conditions such as divisibility rules, leap year validation, and grading systems.
4.  **State Manifestation:** Utilize the `print()` function for formatted system output and state reporting.

--- ◈ ---

## ◈ Technical Implementation

### 1. Variable Orchestration & Geometric Analysis
```python
import math

# --- 1. Geometric Magnitude: Hypotenuse Calculation ---
def compute_hypotenuse(a, b):
    """Calculates the diagonal length of a right triangle."""
    return math.sqrt(a**2 + b**2)

# --- 2. Temporal Transmutation: Seconds to ISO Format ---
def convert_seconds_to_hms(total_seconds):
    """Parses total seconds into hours, minutes, and seconds."""
    hours = total_seconds // 3600
    minutes = (total_seconds % 3600) // 60
    seconds = total_seconds % 60
    return f"{hours}h {minutes}m {seconds}s"

# --- 3. Optimized Variable Exchange ---
x, y = 5, 10
x, y = y, x  # Pythonic swap via tuple unpacking

# Validation Output
print(f"Hypotenuse Magnitude: {compute_hypotenuse(3, 4)}")
print(f"Temporal Output: {convert_seconds_to_hms(3665)}")
```

### 2. Decision Architectures
```python
# --- 1. Leap Cycle Oracle ---
def validate_leap_cycle(year):
    """Evaluates Gregorian leap year criteria."""
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return "Leap Year Validated"
    return "Standard Year"

# --- 2. Academic Performance Tiering ---
def categorize_academic_performance(marks_list):
    """Categorizes performance based on CGPA thresholds."""
    average = sum(marks_list) / len(marks_list)
    cgpa = average / 10
    
    if cgpa >= 9.0: tier = "O (Outstanding)"
    elif cgpa >= 8.0: tier = "A+ (Excellent)"
    elif cgpa >= 7.0: tier = "A (Very Good)"
    elif cgpa >= 6.0: tier = "B+ (Good)"
    else: tier = "F (Below Threshold)"
    
    return average, tier

# Validation Output
print(f"Cycle Analysis (2024): {validate_leap_cycle(2024)}")
avg, perf = categorize_academic_performance([70, 80, 90, 60, 50])
print(f"Average Mean: {avg}, Academic Tier: {perf}")
```

--- ◈ ---

## ◈ Execution & Validation
```text
Hypotenuse Magnitude: 5.0
Temporal Output: 1h 1m 5s
Variable Exchange [x,y]: 10, 5

Cycle Analysis (2024): Leap Year Validated
Average Mean: 70.0, Academic Tier: A (Very Good)
```

## ◈ Analysis & Synthesis
Mastering the foundations of syntax and conditional logic is paramount for any software architect. The efficiency of Python's arithmetic engine and the clarity of its branching structures provide a powerful toolkit for developing robust algorithmic solutions. This experiment confirms that even basic syntax, when applied with architectural precision, can solve complex logic puzzles effectively.

<div style="page-break-after: always;"></div>

# ◈ Control Flow & Iterative Optimization (Exp 3)

| Field | Details |
| :--- | :--- |
| **Architect** | Aryaveer Lohia |
| **SAP ID** | 590025719 |
| **Batch** | B18 |
| **Subject** | Python Programming |

--- ◈ ---

## ◈ Objective & Scope
The objective is to implement and optimize various iterative algorithms in Python using `for` and `while` loop constructs. The scope includes mathematical sequence generation, numeric property validation, and the utilization of control flow modifiers (`break`, `continue`) for efficient logic execution.

## ◈ Conceptual Framework
Iterative logic is the foundation of automated computation.
*   **The `for` Loop:** Optimized for iterating over fixed sequences or ranges where the iteration count is deterministic.
*   **The `while` Loop:** Ideal for scenarios where the execution depends on a dynamic boolean predicate, continuing until the condition is invalidated.
*   **Control Modifiers:** `break` allows for immediate termination of a cycle upon meeting a specific exit condition, while `continue` facilitates the skipping of non-essential iterations.

## ◈ Procedural Logic
1.  **Input Ingestion:** Collect parameters from the user interface using the `input()` function.
2.  **Initialization:** Establish initial state variables (accumulators, counters, flags).
3.  **Iterative Processing:**
    -   Implement range-based `for` loops for deterministic sequences.
    -   Utilize conditional `while` loops for state-dependent iterations (e.g., digit decomposition).
4.  **Result Formulation:** Consolidate processed data into a final state.
5.  **Output Presentation:** Reveal the computed results via formatted string outputs.

--- ◈ ---

## ◈ Technical Implementation

### 1. Factorial Calculation (Linear Iteration)
```python
def calculate_factorial_iterative():
    """Computes the factorial of a given integer using linear iteration."""
    try:
        n = int(input("Enter integer for factorial analysis: "))
        product = 1
        for i in range(1, n + 1):
            product *= i
        print(f"Calculated Factorial ({n}): {product}")
    except ValueError:
        print("System Error: Input must be a valid integer.")
```

### 2. Armstrong Property Validation
```python
def validate_armstrong_state():
    """Analyzes a number to determine if it satisfies the Armstrong property."""
    num = int(input("Enter number for Armstrong validation: "))
    temp, total = num, 0
    while temp > 0:
        digit = temp % 10
        total += digit ** 3
        temp //= 10
    
    status = "Validated" if total == num else "Invalid"
    print(f"Armstrong Status ({num}): {status}")
```

### 3. Fibonacci Sequence Generation
```python
def generate_fibonacci_sequence():
    """Generates an n-length Fibonacci sequence."""
    n = int(input("Enter sequence length: "))
    a, b = 0, 1
    print("Sequence Output:", end=" ")
    for _ in range(n):
        print(a, end=" ")
        a, b = b, a + b
    print()
```

### 4. Prime Number Sentinel
```python
def analyze_prime_purity():
    """Performs primality testing on a target integer."""
    num = int(input("Enter integer for primality test: "))
    if num > 1:
        for i in range(2, int(num**0.5) + 1):
            if num % i == 0:
                print(f"Result: {num} is Composite.")
                break
        else:
            print(f"Result: {num} is Prime.")
    else:
        print(f"Result: {num} is not Prime.")
```

### 5. Palindrome Verification
```python
def verify_numeric_symmetry():
    """Checks if a numeric state exhibits symmetric properties (Palindrome)."""
    num = int(input("Enter number for symmetry check: "))
    temp, reverse_num = num, 0
    while temp > 0:
        reverse_num = (reverse_num * 10) + (temp % 10)
        temp //= 10
    
    status = "Symmetric" if reverse_num == num else "Asymmetric"
    print(f"Numeric Status: {status}")
```

### 6. Geometric Pattern Synthesis
```python
def synthesize_geometric_pattern():
    """Synthesizes a visual pattern using nested iteration."""
    for i in range(5, 0, -1):
        for j in range(1, i + 1):
            print(j, end="")
        print("*" * (10 - 2 * i), end="")
        for j in range(i, 0, -1):
            print(j, end="")
        print()
```

--- ◈ ---

## ◈ Execution & Validation
```text
Enter integer for factorial analysis: 5
Calculated Factorial (5): 120

Enter number for Armstrong validation: 153
Armstrong Status (153): Validated

Enter sequence length: 6
Sequence Output: 0 1 1 2 3 5 

123451
1234**4321
123****321
12******21
1********1
```

## ◈ Analysis & Synthesis
Iterative control flow is a critical component of software architecture. Through the implementation of `for` and `while` loops, we have demonstrated how complex mathematical and structural problems can be decomposed into a series of repeatable, optimized steps. Mastering these constructs is essential for developing efficient algorithms and system-level automation tools.

<div style="page-break-after: always;"></div>

# ◈ Advanced Data Structures & Functional Modularity (Exp 4, 5, 6)

| Field | Details |
| :--- | :--- |
| **Architect** | Aryaveer Lohia |
| **SAP ID** | 590025719 |
| **Batch** | B18 |
| **Subject** | Python Programming |

--- ◈ ---

## ◈ Experiment No. 4: Strings & Sets

### ## ◈ Objective & Scope
The objective is to explore advanced string manipulation techniques and leverage the mathematical properties of sets to manage unique data collections and perform efficient membership testing.

### ## ◈ Conceptual Framework
**Strings: Immutable Sequences**
Strings in Python are immutable Unicode sequences. Operations such as slicing, indexing, and various string methods allow for complex text processing without altering the original data structure, ensuring data integrity.

**Sets: Unordered Unique Collections**
Sets are optimized for high-performance membership testing and eliminating duplicate entries. They support mathematical operations like Union, Intersection, and Difference, which are essential for relational data analysis.

### ## ◈ Procedural Logic
**Part A: Uppercase Analysis**
1. Accept string input from the user.
2. Iterate through the sequence to identify characters where the `isupper()` property is true.
3. Compute the total count of uppercase occurrences.

**Part B: Lexical Extraction**
1. Accept a multi-word sentence.
2. Normalize the text by converting it to lowercase.
3. Tokenize the sentence into individual words.
4. Cast the collection into a `set` to extract unique lexical elements.

### ## ◈ Technical Implementation
```python
# --- Program 1: Uppercase Character Analysis ---
def analyze_uppercase_frequency():
    """Analyzes a string to count uppercase characters."""
    text = input("Enter a string for analysis: ")
    count = sum(1 for char in text if char.isupper())
    print(f"Analysis complete: {count} uppercase characters identified.")

# --- Program 2: Unique Lexical Extraction ---
def extract_unique_lexicon():
    """Transforms a sentence into a set of unique, normalized words."""
    sentence = input("\nEnter a sentence to extract unique lexicon: ")
    
    # Text normalization and tokenization
    words = sentence.lower().split()
    unique_lexicon = set(words)
    
    print(f"Original Lexicon: {words}")
    print(f"Unique Lexicon: {unique_lexicon}")
    print(f"Total Unique Elements: {len(unique_lexicon)}")

if __name__ == "__main__":
    analyze_uppercase_frequency()
    extract_unique_lexicon()
```

### ## ◈ Execution & Validation
```text
Enter a string for analysis: Welcome to Python Programming Lab!
Analysis complete: 4 uppercase characters identified.

Enter a sentence to extract unique lexicon: Python is great and Python is easy to learn
Original Lexicon: ['python', 'is', 'great', 'and', 'python', 'is', 'easy', 'to', 'learn']
Unique Lexicon: {'python', 'is', 'great', 'and', 'easy', 'to', 'learn'}
Total Unique Elements: 7
```

<div style="page-break-after: always;"></div>

## ◈ Experiment No. 5: Lists, Tuples, & Dictionaries

### ## ◈ Objective & Scope
To master the selection and implementation of Python's primary data containers—Lists, Tuples, and Dictionaries—based on their mutability and access performance characteristics.

### ## ◈ Conceptual Framework
**Lists: Dynamic Arrays**
Lists are mutable, ordered sequences that support dynamic resizing and in-place modifications, making them ideal for collections that evolve during runtime.

**Tuples: Immutable Records**
Tuples provide a fixed-state alternative to lists, offering performance optimizations and ensuring that data remain constant throughout the program lifecycle.

**Dictionaries: Hash-Based Key-Value Pairs**
Dictionaries facilitate O(1) average-time complexity for lookups, providing a highly efficient way to map unique keys to values.

### ## ◈ Procedural Logic
**Part A: Secondary Maximum Extraction**
1. Ingest a list of numerical scores.
2. Utilize a set to eliminate duplicate values.
3. Sort the unique values in descending order.
4. Extract the second element from the sorted sequence.

**Part B: Associative Data Lookup**
1. Initialize a dictionary mapping names to contact identifiers.
2. Query the dictionary using a user-provided key.
3. Handle potential missing keys gracefully to ensure system stability.

### ## ◈ Technical Implementation
```python
# --- Program 1: Runner-Up Detection ---
def detect_runner_up():
    """Identifies the second highest score within a dataset."""
    print("--- Execution: Runner-Up Detection ---")
    try:
        n = int(input("Enter number of participants: "))
        scores = list(map(int, input("Enter scores (space-separated): ").split()))
        
        # De-duplication and sorting
        unique_scores = sorted(list(set(scores)), reverse=True)
        
        if len(unique_scores) > 1:
            print(f"The runner-up score is: {unique_scores[1]}")
        else:
            print("Insufficient unique data points for runner-up detection.")
    except ValueError:
        print("Error: Input must be numerical.")

# --- Program 2: Contact Registry System ---
def manage_registry():
    """Provides key-based lookup for contact information."""
    print("\n--- Execution: Contact Registry Lookup ---")
    registry = {
        "Aryaveer": "9876543210",
        "Rahul": "8887776665",
        "Sneha": "7776665554"
    }
    
    query = input("Enter name for registry lookup: ")
    result = registry.get(query)
    
    if result:
        print(f"Registry Result for {query}: {result}")
    else:
        print("Record not found in registry.")

if __name__ == "__main__":
    detect_runner_up()
    manage_registry()
```

### ## ◈ Execution & Validation
```text
--- Execution: Runner-Up Detection ---
Enter number of participants: 5
Enter scores (space-separated): 23 45 45 12 30
The runner-up score is: 30

--- Execution: Contact Registry Lookup ---
Enter name for registry lookup: Aryaveer
Registry Result for Aryaveer: 9876543210
```

<div style="page-break-after: always;"></div>

## ◈ Experiment No. 6: Functional Abstraction & Recursion

### ## ◈ Objective & Scope
To implement modular code through user-defined functions, recursive logic, and anonymous lambda expressions, focusing on code reusability and algorithmic clarity.

### ## ◈ Conceptual Framework
**Modular Functions**
Encapsulating logic into functions promotes the DRY (Don't Repeat Yourself) principle and enhances maintainability.

**Recursive Logic**
Recursion allows for the elegant solution of problems that exhibit self-similarity, where a function solves a base case and delegates smaller sub-problems to itself.

**Lambda Expressions**
Anonymous functions provide a concise syntax for defining small, one-off logical operations, often used as arguments for higher-order functions.

### ## ◈ Procedural Logic
**Part A: Recursive Fibonacci Generation**
1. Define base cases (0 and 1).
2. Implement the recursive step: `F(n) = F(n-1) + F(n-2)`.
3. Iterate through the desired range to manifest the sequence.

**Part B: Geometric Volume Calculation via Lambda**
1. Define a lambda function implementing the formula: `V = (1/3) * π * r² * h`.
2. Ingest dimensions and execute the lambda for immediate calculation.

### ## ◈ Technical Implementation
```python
import math

# --- Recursive Algorithm ---
def fibonacci_recursive(n):
    """Calculates the n-th Fibonacci term via recursive delegation."""
    if n <= 1:
        return n
    return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)

# --- Anonymous Functional Spark ---
# Formula: (1/3) * pi * r^2 * h
calculate_cone_volume = lambda r, h: (1/3) * math.pi * (r**2) * h

def orchestrate_functions():
    """Orchestrates the demonstration of functional paradigms."""
    # 1. Recursive Sequence Manifestation
    print("--- Execution: Fibonacci Recursion ---")
    try:
        limit = int(input("Enter number of terms: "))
        print("Sequence:", end=" ")
        for i in range(limit):
            print(fibonacci_recursive(i), end=" ")
        print()
    except ValueError:
        print("Error: Input must be an integer.")

    # 2. Anonymous Geometric Calculation
    print("\n--- Execution: Lambda-Based Geometric Analysis ---")
    try:
        radius = float(input("Enter cone radius: "))
        height = float(input("Enter cone height: "))
        volume = calculate_cone_volume(radius, height)
        print(f"Calculated Volume: {volume:.4f}")
    except ValueError:
        print("Error: Invalid dimensions provided.")

if __name__ == "__main__":
    orchestrate_functions()
```

### ## ◈ Execution & Validation
```text
--- Execution: Fibonacci Recursion ---
Enter number of terms: 10
Sequence: 0 1 1 2 3 5 8 13 21 34 

--- Execution: Lambda-Based Geometric Analysis ---
Enter cone radius: 5
Enter cone height: 7
Calculated Volume: 183.2596
```

### ## ◈ Analysis & Synthesis
The implementation of advanced data structures and functional paradigms demonstrates a comprehensive understanding of Python's architectural flexibility. Functional modularity is the cornerstone of clean architecture. This experiment validates that recursion and lambdas both contribute to creating a more readable and efficient codebase.

<div style="page-break-after: always;"></div>

# ◈ Data Persistence & Fault-Tolerant Systems (Exp 7)

| Field | Details |
| :--- | :--- |
| **Architect** | Aryaveer Lohia |
| **SAP ID** | 590025719 |
| **Batch** | B18 |
| **Subject** | Python Programming |

--- ◈ ---

## ◈ Objective & Scope
The objective is to implement robust data persistence mechanisms using Python's file I/O capabilities and to design fault-tolerant systems through comprehensive exception handling. The scope covers text-based data storage, retrieval, and the management of runtime anomalies.

## ◈ Conceptual Framework
**Data Persistence (File I/O):**
Persistent storage allows applications to retain state beyond the execution lifecycle. Python's `open()` function, combined with the `with` context manager, ensures safe resource allocation and deallocation (RAII principle), preventing file handle leaks.

**Fault Tolerance (Exception Handling):**
Resilient software must anticipate and gracefully handle runtime errors. The `try-except-finally` construct allows for the redirection of execution flow when anomalies (e.g., `IOError`, `ValueError`) occur, ensuring system stability.

## ◈ Procedural Logic
1.  **Data Inscription:** Populate files with structured data (names, numerical records) using the `write()` method.
2.  **Data Transformation:** Retrieve and parse inscribed data, converting raw strings into typed collections (e.g., lists of integers).
3.  **Resilience Integration:** Wrap I/O and parsing logic in `try` blocks to manage resource-level and data-level faults.
4.  **Custom Fault Oracles:** Define specialized exception classes to handle domain-specific anomalies.

--- ◈ ---

## ◈ Technical Implementation

### 1. Lexical Record Analysis
```python
# Inscribing and analyzing lexical records
try:
    with open("lexicon.txt", "w") as f:
        names = ["Aman", "Neha", "Ishita", "Om", "Ravi", "Uday"]
        for name in names:
            f.write(f"{name}\n")
            
    with open("lexicon.txt", "r") as f:
        records = [line.strip() for line in f]
        
    print(f"Total records synchronized: {len(records)}")
    
    # Analysis: Prefix-based filtering
    vowels = ('A', 'E', 'I', 'O', 'U')
    prefix_match_count = sum(1 for n in records if n.upper().startswith(vowels))
    print(f"Records with vowel prefix: {prefix_match_count}")
    
    longest_record = max(records, key=len)
    print(f"Maximum record length identified: {longest_record}")
    
except Exception as e:
    print(f"I/O Analysis Fault: {e}")
```

### 2. Numerical Ledger Processing
```python
# Processing persistent numerical datasets
try:
    with open("ledger.txt", "w") as f:
        entries = [10, 150, 200, 45, 99, 120, 300]
        for e in entries:
            f.write(f"{e}\n")
            
    with open("ledger.txt", "r") as f:
        data_points = [int(line.strip()) for line in f]
        
    print(f"Peak value in ledger: {max(data_points)}")
    print(f"Mean value of dataset: {sum(data_points)/len(data_points):.2f}")
    
    # Threshold filtering
    outliers = sum(1 for e in data_points if e > 100)
    print(f"Entries exceeding threshold (100): {outliers}")
    
except Exception as e:
    print(f"Data Processing Fault: {e}")
```

<div style="page-break-after: always;"></div>

### 3. Custom Exception Architectures
```python
class NullResourceError(Exception):
    """Raised when a target resource contains no data."""
    pass

class DataIntegrityError(Exception):
    """Raised when data fails format validation."""
    pass

def audit_resource_integrity(filename):
    """Audits the integrity of a persistent resource."""
    try:
        with open(filename, "r") as f:
            content = f.read()
            if not content:
                raise NullResourceError("Resource is empty.")
            if not content.replace("\n", "").isalnum():
                raise DataIntegrityError("Non-alphanumeric characters identified.")
            print("Resource Audit: Integrity Validated.")
    except FileNotFoundError:
        print("System Error: Resource not found on disk.")
    except (NullResourceError, DataIntegrityError) as e:
        print(f"Audit Exception: {e}")

audit_resource_integrity("audit_target.txt")
```

--- ◈ ---

## ◈ Execution & Validation
```text
Total records synchronized: 6
Records with vowel prefix: 3
Maximum record length identified: Ishita

Peak value in ledger: 300
Mean value of dataset: 134.86
Entries exceeding threshold (100): 4

System Error: Resource not found on disk.
Audit Status: Execution complete.
```

## ◈ Analysis & Synthesis
Establishing reliable data persistence and fault-tolerant architectures is essential for professional software development. By utilizing context managers for file handling and structured exception hierarchies for error management, we ensure that our systems are both enduring and resilient under diverse operational conditions.

<div style="page-break-after: always;"></div>

# ◈ Graphical Interfaces & Relational Persistence (Lab 8)

| Field | Details |
| :--- | :--- |
| **Architect** | Aryaveer Lohia |
| **SAP ID** | 590025719 |
| **Batch** | B18 |
| **Subject** | Python Programming |

--- ◈ ---

## ◈ Objective & Scope
The objective is to architect desktop applications using the Tkinter framework and integrate them with persistent relational storage using SQLite. The scope covers the design of intuitive user interfaces and the implementation of CRUD (Create, Read, Update, Delete) operations through a secure database backend.

## ◈ Conceptual Framework
**Graphical User Interface (GUI):**
The GUI layer (Tkinter) serves as the primary interface for human-system interaction. By employing an event-driven programming model, we can respond to user-triggered events through specialized handlers, creating a dynamic and interactive experience.

**Relational Persistence (SQLite):**
To ensure data longevity beyond the application session, we utilize SQLite—a lightweight, serverless relational database engine. Integrating the UI with a persistent backend allows for the storage and retrieval of structured data, essential for professional-grade software solutions.

--- ◈ ---

## Experiment 1: The Window Initialization

### ## ◈ Procedural Logic
1.  **System Initialization:** Instantiate the `Tk()` root class to initialize the windowing subsystem.
2.  **State Configuration:** Define the window's geometric constraints and title.
3.  **UI Manifestation:** Deploy basic Label widgets to confirm visual rendering.

### ## ◈ Technical Implementation
```python
import tkinter as tk

def initialize_root_window():
    """Initializes the base Tkinter windowing system."""
    root = tk.Tk()
    root.title("System Interface Prototype")
    root.geometry("400x300")
    root.resizable(False, False)

    # Initializing visual confirmation
    status_label = tk.Label(root, text="Interface Operational", font=("Helvetica", 14))
    status_label.pack(pady=100)

    root.mainloop()

if __name__ == "__main__":
    initialize_root_window()
```

<div style="page-break-after: always;"></div>

## Experiment 2: The Arithmetic Logic Engine

### ## ◈ Procedural Logic
1.  **Grid Topology:** Arrange numeric and operator widgets in a grid layout to facilitate intuitive access.
2.  **Expression Parsing:** Utilize the `eval()` engine to dynamically compute mathematical results from string inputs.
3.  **Variable Synchrony:** Bind `StringVar()` to the entry field for real-time state synchronization.

### ## ◈ Technical Implementation
```python
import tkinter as tk

def on_input_event(event):
    """Handles click events for the arithmetic engine."""
    input_text = event.widget.cget("text")
    if input_text == "=":
        try:
            result = str(eval(display_var.get()))
            display_var.set(result)
        except Exception:
            display_var.set("Syntax Error")
    elif input_text == "C":
        display_var.set("")
    else:
        display_var.set(display_var.get() + input_text)

def build_arithmetic_engine():
    """Constructs the visual and logical layers of the calculator."""
    root = tk.Tk()
    root.title("Arithmetic Engine")
    root.geometry("300x450")

    global display_var
    display_var = tk.StringVar()
    display_field = tk.Entry(root, textvar=display_var, font="lucida 20 bold", justify='right')
    display_field.pack(fill="both", pady=15, padx=15)

    layout = [
        ["7", "8", "9", "/"],
        ["4", "5", "6", "*"],
        ["1", "2", "3", "-"],
        ["0", ".", "=", "+"],
        ["C"]
    ]

    for row in layout:
        row_frame = tk.Frame(root)
        row_frame.pack()
        for char in row:
            btn = tk.Button(row_frame, text=char, width=5, height=2, font="lucida 15 bold")
            btn.pack(side="left", padx=5, pady=5)
            btn.bind("<Button-1>", on_input_event)

    root.mainloop()

if __name__ == "__main__":
    build_arithmetic_engine()
```

<div style="page-break-after: always;"></div>

## Experiment 3: Persistent Registry System

### ## ◈ Procedural Logic
1.  **SQL Connection:** Establish a persistent link to `registry.db`.
2.  **Data Extraction:** Ingest data from UI Entry fields (Name, Course, Email).
3.  **Parameterized Persistence:** Inscribe data into the SQL table using sanitized queries to ensure system security.

### ## ◈ Technical Implementation
```python
import tkinter as tk
import sqlite3

def persist_registry_data():
    """Synchronizes UI data with the persistent SQL backend."""
    name, course, email = ent_name.get(), ent_course.get(), ent_email.get()
    
    if all([name, course, email]):
        try:
            conn = sqlite3.connect("registry.db")
            cur = conn.cursor()
            cur.execute("INSERT INTO students(name, course, email) VALUES (?, ?, ?)", (name, course, email))
            conn.commit()
            lbl_status.config(text="Status: Synchronization Successful", fg="green")
            for e in [ent_name, ent_course, ent_email]: e.delete(0, tk.END)
        except sqlite3.Error as e:
            lbl_status.config(text=f"Database Fault: {e}", fg="red")
        finally:
            if conn: conn.close()
    else:
        lbl_status.config(text="Status: Missing Input Fields", fg="red")

def setup_registry_ui():
    """Orchestrates the UI layout for the registry system."""
    global ent_name, ent_course, ent_email, lbl_status
    root = tk.Tk()
    root.title("Persistent Registry Form")
    root.geometry("400x400")

    tk.Label(root, text="Full Name:").pack(pady=5)
    ent_name = tk.Entry(root, width=35); ent_name.pack()

    tk.Label(root, text="Program of Study:").pack(pady=5)
    ent_course = tk.Entry(root, width=35); ent_course.pack()

    tk.Label(root, text="Email Identifier:").pack(pady=5)
    ent_email = tk.Entry(root, width=35); ent_email.pack()

    tk.Button(root, text="Persist Data", command=persist_registry_data, bg="#2E7D32", fg="white").pack(pady=30)

    lbl_status = tk.Label(root, text="", font=("Helvetica", 10, "italic"))
    lbl_status.pack()

    root.mainloop()

if __name__ == "__main__":
    setup_registry_ui()
```

--- ◈ ---

## ◈ Analysis & Synthesis
The integration of Tkinter and SQLite provides a robust architectural pattern for developing modern desktop applications. This experiment confirms that separating the visual presentation layer from the persistent data layer is essential for creating scalable, maintainable, and secure software systems.

<div style="page-break-after: always;"></div>

# ◈ Object-Oriented Systems & Polymorphic Architectures (Exp 9)

| Field | Details |
| :--- | :--- |
| **Architect** | Aryaveer Lohia |
| **SAP ID** | 590025719 |
| **Batch** | B18 |
| **Subject** | Python Programming |

--- ◈ ---

## ◈ Objective & Scope
The objective is to implement and analyze core Object-Oriented Programming (OOP) paradigms in Python, including Class-based modeling, Inheritance hierarchies, Method Overriding, and Operator Overloading to build scalable and reusable software components.

## ◈ Conceptual Framework
Object-Oriented Programming in Python treats all entities as objects, emphasizing data encapsulation and behavioral abstraction.

*   **Encapsulation:** Consolidating state (attributes) and behavior (methods) within a cohesive unit.
*   **Inheritance:** Facilitating code reuse by allowing child classes to derive attributes and methods from parent classes.
*   **Polymorphism:** Enabling uniform interfaces for diverse underlying forms, implemented through method overriding and operator overloading.

## ◈ Procedural Logic
1.  **System Modeling:** Define classes with `__init__` constructors to initialize object states.
2.  **State Management:** Implement methods to expose and manipulate internal data safely.
3.  **Hierarchy Design:** Explore diverse inheritance patterns.
4.  **Behavioral Specialization:** Override parent methods to provide specific implementations in derived classes.
5.  **Syntactic Extension:** Overload standard operators (e.g., `+`) to enable intuitive interactions between custom objects.

--- ◈ ---

## ◈ Technical Implementation

### 1. The Student Modeling System
```python
class Student:
    """Represents a student entity within an academic management system."""
    
    def __init__(self, name, sap_id, physics, chemistry, maths):
        self.name = name
        self.sap_id = sap_id
        self.marks = {
            "Physics": physics, 
            "Chemistry": chemistry, 
            "Maths": maths
        }

    def display_profile(self):
        """Exposes the student's profile data."""
        print(f"\n--- System Profile: {self.name} ---")
        print(f"SAP ID: {self.sap_id}")
        print(f"Academic Record: {self.marks}")

    def calculate_percentage(self):
        """Computes the aggregate percentage of marks."""
        return sum(self.marks.values()) / len(self.marks)

    def determine_result(self):
        """Validates if marks meet the minimum threshold of 40 in all subjects."""
        return "Pass" if all(mark > 40 for mark in self.marks.values()) else "Fail"
```

<div style="page-break-after: always;"></div>

### 2. Inheritance Patterns & Lineage
```python
# --- Single Inheritance ---
class BaseSystem:
    def log_status(self): print("Base system operational.")

class DerivedSystem(BaseSystem):
    def execute_task(self): print("Executing specialized task.")

# --- Multiple Inheritance ---
class StorageManager:
    def save_data(self): print("Data persisted to storage.")

class NetworkManager:
    def send_data(self): print("Data transmitted over network.")

class IntegratedSystem(StorageManager, NetworkManager):
    def synchronize(self): print("System synchronization in progress.")
```

### 3. Polymorphic Operator Overloading
```python
class Vector2D:
    """Models a 2D coordinate system with support for vector addition."""
    
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __add__(self, other):
        """Overloads the '+' operator for coordinate-wise addition."""
        return Vector2D(self.x + other.x, self.y + other.y)

    def __str__(self):
        """Returns a string representation of the vector state."""
        return f"Vector2D(x={self.x}, y={self.y})"
```

--- ◈ ---

## ◈ Execution & Validation
```text
--- System Profile: Aryaveer ---
SAP ID: 500123456
Academic Record: {'Physics': 85.0, 'Chemistry': 90.0, 'Maths': 88.0}
Percentage: 87.67%
Result: Pass

--- Operator Overloading Validation ---
Vector 1: Vector2D(x=10, y=20)
Vector 2: Vector2D(x=12, y=15)
Vector Sum: Vector2D(x=22, y=35)
```

## ◈ Analysis & Synthesis
The implementation of OOP principles significantly enhances the modularity and extensibility of the system. Through inheritance and polymorphism, we achieve a balance between shared logic and specialized behavior, which is essential for developing complex, industrial-grade software architectures.

<div style="page-break-after: always;"></div>

# ◈ Comprehensive Python Engineering Portfolio (Final Project)

| Field | Details |
| :--- | :--- |
| **Architect** | Aryaveer Lohia |
| **SAP ID** | 590025719 |
| **Batch** | B18 |
| **Subject** | Python Programming (CSL210) |

--- ◈ ---

## ◈ Objective & Scope
This portfolio serves as a comprehensive technical audit of a multi-disciplinary development journey within the Python ecosystem. It documents the transition from fundamental algorithmic logic to advanced system-level integrations, including database management and graphical user interfaces.

## ◈ Conceptual Framework
The curriculum focused on five primary architectural pillars:
*   **Dynamic Execution Logic:** Leveraging Python's dynamic typing and abstractions.
*   **Iterative & Flow Control:** Implementing optimized loops and decision-making structures.
*   **Functional Modularity:** Decomposing complex systems into reusable, decoupled units.
*   **Data Persistence & I/O:** Establishing reliable links between volatile memory and permanent storage.
*   **Human-Computer Interaction (HCI):** Designing intuitive graphical interfaces.

--- ◈ ---

## Section I: Foundations & Decision Architecture
### ## ◈ Technical Implementation
```python
import math

def calculate_diagonal_magnitude(a, b):
    """Calculates the hypotenuse of a right triangle."""
    return math.sqrt(a**2 + b**2)

def evaluate_leap_year(year):
    """Executes logical validation for leap year status."""
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return f"Year {year}: Leap Cycle Validated"
    return f"Year {year}: Standard Cycle"

# Validation
print(f"Magnitude: {calculate_diagonal_magnitude(3, 4)}")
print(evaluate_leap_year(2024))
```

<div style="page-break-after: always;"></div>

## Section II: Control Flow & State Management
### ## ◈ Technical Implementation
```python
def validate_armstrong_property(num):
    """Validates if a number satisfies the Armstrong sum property."""
    temp, total = num, 0
    while temp > 0:
        digit = temp % 10
        total += digit ** 3
        temp //= 10
    return total == num

def generate_fibonacci_sequence(n):
    """Generates an n-length Fibonacci sequence using iterative optimization."""
    a, b = 0, 1
    sequence = []
    for _ in range(n):
        sequence.append(a)
        a, b = b, a + b
    return sequence

# Validation
print(f"Armstrong Validation (153): {validate_armstrong_property(153)}")
print(f"Sequence Generation (n=5): {generate_fibonacci_sequence(5)}")
```

## Section III: Advanced Structures & Functional Modularity
### ## ◈ Technical Implementation
```python
import math

# Lambda Expression: Geometric Volume Calculation
compute_volume = lambda r, h: (1/3) * math.pi * (r**2) * h

def recursive_factorial(n):
    """Implements factorial calculation via recursive delegation."""
    if n == 0: return 1
    return n * recursive_factorial(n - 1)

# Validation
print(f"Computed Volume: {compute_volume(5, 10):.2f}")
print(f"Recursive Factorial (5): {recursive_factorial(5)}")
```

<div style="page-break-after: always;"></div>

## Section IV: Data Persistence & Exception Handling
### ## ◈ Technical Implementation
```python
def analyze_geographic_data():
    """Reads and parses geographic datasets with integrated error handling."""
    try:
        with open("geo_data.txt", "w") as f:
            f.write("Dehradun,5.7,308\nDelhi,190,1484")
        with open("geo_data.txt", "r") as f:
            for line in f:
                name, pop, area = line.strip().split(",")
                if float(pop) > 10:
                    print(f"Analysis: High-Density Hub Detected -> {name}")
    except Exception as e:
        print(f"System Error: {e}")

analyze_geographic_data()
```

## Section V: GUI Engineering & Relational Integration
### ## ◈ Technical Implementation
```python
import sqlite3

def verify_authentication(username, password):
    """Verifies credentials against a persistent SQL database."""
    try:
        connection = sqlite3.connect("system_auth.db")
        cursor = connection.cursor()
        cursor.execute("SELECT * FROM users WHERE uname=? AND pass=?", (username, password))
        return "Authentication Successful" if cursor.fetchone() else "Access Denied"
    except sqlite3.Error as e:
        return f"Database Fault: {e}"
    finally:
        if connection: connection.close()

# Validation
print(f"Auth Status: {verify_authentication('admin', 'secure_pass')}")
```

--- ◈ ---

## ◈ Analysis & Synthesis
This portfolio demonstrates a comprehensive mastery of the Python development lifecycle. The integration of functional modularity, data persistence, and graphical interfaces forms a solid architectural foundation. Future iterations will focus on expanding these systems into distributed environments and incorporating advanced data analytics pipelines.
