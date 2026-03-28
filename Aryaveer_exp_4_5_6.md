# Technical Report: Advanced Data Structures & Functional Modularity (Exp 4, 5, 6)

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

### ## ◈ Analysis & Synthesis
The implementation demonstrates the efficiency of using sets for de-duplication and the utility of string methods for content analysis. These structures form the basis for more complex text processing and data normalization tasks.

<div style="page-break-after: always;"></div>

--- ◈ ---

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

### ## ◈ Analysis & Synthesis
Selecting the appropriate data structure is critical for architectural performance. This experiment highlights the trade-offs between mutability and lookup efficiency, demonstrating how dictionaries and sets can significantly optimize data retrieval.

<div style="page-break-after: always;"></div>

--- ◈ ---

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
Functional modularity is the cornerstone of clean architecture. This experiment validates that recursion and lambdas, while different in syntax and execution, both contribute to creating a more readable and efficient codebase.
