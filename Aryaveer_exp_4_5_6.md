# Lab Report: Python Programming

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiment   :** Strings, Sets, Data Structures, and Functions (Experiments 4, 5, & 6)  

---

## Experiment No. 4: Strings and Sets

### 1. Aim
To explore string manipulation techniques and set operations in Python.

### 2. Theory
**Strings:** In Python, strings are immutable sequences of characters. They support a variety of methods for searching, splitting, and case modification.
**Sets:** A set is an unordered collection of unique elements. Sets are useful for removing duplicates and performing mathematical operations like union and intersection.

### 3. Algorithm / Steps
1.  **String Analysis:** Iterate through strings to count specific character types (uppercase, vowels, etc.) using boolean methods like `.isupper()`.
2.  **Word Processing:** Use `.split()` to break sentences into lists of words.
3.  **Set Logic:** Use `set()` to filter unique items and operators like `&`, `|`, and `-` for set math.

### 4. Program Code Snippets (Selected)
```python
# Count Capital Letters
s = input("Enter a string: ")
count = sum(1 for ch in s if ch.isupper())
print("Number of capital letters:", count)

# Unique Words using Set
sentence = input("Enter a sentence: ")
unique_words = set(sentence.lower().split())
print("Number of unique words:", len(unique_words))
```

### 5. Output
```bash
PS C:\Users\lohia> python exp4.py
Enter a string: Hello World
Number of capital letters: 2

PS C:\Users\lohia> python unique_words.py
Enter a sentence: Python is fun and Python is powerful
Number of unique words: 5
```

---

## Experiment No. 5: Lists, Tuples, and Dictionaries

### 1. Aim
To implement and manage complex data structures including lists, tuples, and dictionaries.

### 2. Theory
**Lists:** Mutable, ordered sequences.
**Tuples:** Immutable, ordered sequences.
**Dictionaries:** Key-value pairs allowing fast lookups.

### 3. Algorithm / Steps
1.  **List Ops:** Store user inputs in a list and perform aggregations.
2.  **Tuples:** Convert lists to tuples to ensure data integrity.
3.  **Dictionaries:** Map entities (like persons or movies) to their attributes using keys.

### 4. Program Code Snippets (Selected)
```python
# Runner-Up Score
n = int(input("Enter number of scores: "))
scores = list(map(int, input().split()))
unique_scores = sorted(list(set(scores)), reverse=True)
print("Runner-up score:", unique_scores[1])

# Contact Book
contacts = {}
# (Logic for adding/deleting from dictionary)
```

### 5. Output
```bash
PS C:\Users\lohia> python runner_up.py
Enter number of scores: 5
23 45 45 12 30
Runner-up score: 30
```

---

## Experiment No. 6: Functions in Python

### 1. Aim
To study and implement different types of functions, including recursive and lambda functions.

### 2. Theory
Functions are modular blocks of code. **Recursion** is when a function calls itself. **Lambda functions** are small, anonymous one-line functions defined with the `lambda` keyword.

### 3. Algorithm / Steps
1.  **Standard Functions:** Define with `def` and handle arguments (default, keyword, etc.).
2.  **Recursion:** Define a base case and a recursive step.
3.  **Lambda:** Use for concise logic like volume calculation or filtering.

### 4. Program Code Snippets (Selected)
```python
# Fibonacci using Recursion
def fibonacci(n):
    if n <= 1: return n
    return fibonacci(n-1) + fibonacci(n-2)

# Lambda: Volume of Cone
import math
volume_cone = lambda r, h: (1/3) * math.pi * r**2 * h
print("Volume:", volume_cone(5, 7))
```

### 5. Output
```bash
PS C:\Users\lohia> python functions_lab.py
Fibonacci(5): 5
Volume: 183.25957145940458
```

### 6. Result / Conclusion
In these experiments, I successfully mastered the use of Python's built-in data structures (Strings, Sets, Lists, Tuples, Dictionaries) and learned how to encapsulate logic within various types of functions. This provides a robust foundation for building modular and efficient Python applications.
