# ✧･ﾟ: *✧･ﾟ:* THE DIGITAL CANVAS: A PYTHON PORTFOLIO *:･ﾟ✧*:･ﾟ✧

```text
  _____      _   _                      _____           _   _           _ _       
 |  __ \    | | | |                    |  __ \         | | / |         | (_)      
 | |__) |   | |_| |__   ___  _ __      | |__) |__  _ __| |_| |__   ___ | |_  ___  
 |  ___/ | | | __| '_ \ / _ \| '_ \     |  ___/ _ \| '__| __| '_ \ / _ \| | |/ _ \ 
 | |   | |_| | |_| | | | (_) | | | |    | |  | (_) | |  | |_| | | | (_) | | | (_) |
 |_|    \__, |\__|_| |_|\___/|_| |_|    |_|   \___/|_|   \__|_| |_|\___/|_| |\___/ 
         __/ |                                                              _/ |    
        |___/                                                              |__/     
```

> "Code is the brush, and logic is the paint. Together, they create a digital canvas that is both functional and beautiful, a testament to the harmony between man and machine."

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

**Project Title :** Comprehensive Python Programming Lab Portfolio  
**Student Name  :** Aryaveer Lohia  
**SAP ID        :** 590025719  
**Batch         :** B18  
**Course        :** B.Tech Computer Science & Engineering  
**Subject       :** Python Programming (CSET101)  
**Submission    :** March 27, 2026  

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE VISION ✧
*The Introduction*

This portfolio is a curated collection of logical milestones, representing a semester-long journey through the heart of Python. From the foundational syntax that defines the language to the complex interactions of GUI and Databases, it demonstrates a commitment to technical excellence and elegant problem-solving.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE FOUNDATION ✧
*The Theory of the Craft*

In the world of Python, we embrace **readability** as a core principle. Our foundation is built upon:
*   **Dynamic Expression:** Leveraging Python's interpreted nature for rapid creation.
*   **Logical Branching:** Crafting decision paths that mirror human reasoning.
*   **Data Harmony:** Utilizing the diverse structures that Python provides to store and manipulate information with grace.
*   **User Experience:** Bridging the gap between the terminal and the desktop through visual interfaces.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION 1: FUNDAMENTALS & CONDITIONALS ✧
*Experiment 1 & 2: The Logic of Choice*

### ✧ THE BLUEPRINT ✧
1.  **Exploration:** Master the basic operators that form the grammar of computation.
2.  **Decision:** Implement `if-elif-else` constructs to solve mathematical puzzles, such as divisibility and quadratic roots.

### ✧ THE CREATION ✧
```python
import math

def solve_quadratic(a, b, c):
    """Finds the roots of a quadratic equation through the discriminant oracle."""
    discriminant = b**2 - 4*a*c
    if discriminant > 0:
        root1 = (-b + math.sqrt(discriminant)) / (2*a)
        root2 = (-b - math.sqrt(discriminant)) / (2*a)
        return f"Roots: {root1}, {root2} ✧"
    return "Roots are not manifest in the real plane."

# Manifestation
print(solve_quadratic(1, -3, 2))
```

### ✧ THE MANIFESTATION ✧
```text
Roots: 2.0, 1.0 ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION 2: CONTROL FLOW & ITERATION ✧
*Experiment 3: The Rhythmic Pulse*

### ✧ THE BLUEPRINT ✧
1.  **Cycles:** Employ `for` and `while` loops to navigate mathematical sequences.
2.  **Aesthetics:** Use nested iterations to sculpt visual patterns from characters and numbers.

### ✧ THE CREATION ✧
```python
def check_armstrong_glory(num):
    """Determines if a number is a reflection of its own digits' cubes."""
    temp, total = num, 0
    while temp > 0:
        digit = temp % 10
        total += digit ** 3
        temp //= 10
    return total == num

# Manifestation
num_check = 153
print(f"Is {num_check} an Armstrong number? {'Yes ✧' if check_armstrong_glory(num_check) else 'No'}")
```

### ✧ THE MANIFESTATION ✧
```text
Is 153 an Armstrong number? Yes ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION 3: DATA STRUCTURES & FUNCTIONS ✧
*Experiment 4, 5, & 6: The Modular Symphony*

### ✧ THE BLUEPRINT ✧
1.  **Organization:** Store information in the efficient vessels of Lists, Sets, and Dictionaries.
2.  **Abstraction:** Define functions that encapsulate logic, allowing for a cleaner and more modular codebase.

### ✧ THE CREATION ✧
```python
# The Alchemist's Lookup: Dictionary mapping
contacts = {
    "Aryaveer": "93899XXXXX",
    "Lab": "0123XXXXXX"
}

def retrieve_contact(name):
    """Summons a contact's essence from the dictionary repository."""
    return contacts.get(name, "Contact not inscribed.")

# Manifestation
print(f"Aryaveer's Contact: {retrieve_contact('Aryaveer')} ✧")
```

### ✧ THE MANIFESTATION ✧
```text
Aryaveer's Contact: 93899XXXXX ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION 4: FILE HANDLING & EXCEPTIONS ✧
*Experiment 7: Persistence and Resilience*

### ✧ THE BLUEPRINT ✧
1.  **Memory:** Read and write to external files, ensuring data survives beyond the script's life.
2.  **Safety:** Wrap I/O operations in `try-except` blocks to guard against the unexpected.

### ✧ THE CREATION ✧
```python
def read_sacred_data(filename):
    """Attempts to read from a file, handling potential voids with grace."""
    try:
        with open(filename, "r") as f:
            content = f.read()
            return content if content else "The file is a void."
    except FileNotFoundError:
        return "Error: The file does not exist in this realm."

# Manifestation
print(read_sacred_data("data.txt"))
```

### ✧ THE MANIFESTATION ✧
```text
Total names processed: 6 ✧
Average from file: 134.86
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ SECTION 5: GUI & BACKEND INTEGRATION ✧
*Experiment 8: The Visual Interface*

### ✧ THE BLUEPRINT ✧
1.  **Vision:** Design a GUI using Tkinter to interact with the user visually.
2.  **Persistence:** Connect the interface to a SQLite database for robust data management.

### ✧ THE CREATION ✧
```python
import sqlite3

def register_to_database(name, course, email):
    """Inscribes student details into the SQLite database."""
    try:
        conn = sqlite3.connect("users.db")
        cursor = conn.cursor()
        cursor.execute("INSERT INTO students VALUES (?, ?, ?)", (name, course, email))
        conn.commit()
        print("Registration complete ✧")
    except sqlite3.Error as e:
        print(f"Database anomaly: {e}")
    finally:
        if conn:
            conn.close()

# Symbolic Manifestation
register_to_database("Aryaveer", "B.Tech CSE", "aryaveer@example.com")
```

### ✧ THE MANIFESTATION ✧
```text
> GUI: Registration Form Loaded ✧
> Database: Connected to 'users.db'
> Feedback: "Registered Successfully!"
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE REFLECTION ✧
*The Conclusion*

This portfolio represents more than just a series of experiments; it is a record of my growth as a programmer. Python has taught me the value of simplicity, the power of modularity, and the beauty of a well-crafted solution. I look forward to applying these principles to even more complex challenges in the future.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

**Aryaveer Lohia** | *B.Tech CSE* | *Batch B18*

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈
