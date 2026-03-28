# ✧･ﾟ: *✧･ﾟ:* THE GENESIS OF LOGIC *:･ﾟ✧*:･ﾟ✧

```text
  _____           _   _                    
 |  __ \         | | | |                   
 | |__) |   _  __| |_| |__   ___  _ __     
 |  ___/ | | |/ _` __| '_ \ / _ \| '_ \    
 | |   | |_| | (_| |_| | | | (_) | | | |   
 |_|    \__, |\__,____|_| |_|\___/|_| |_|   
         __/ |                             
        |___/                              
```

> "In the beginning, there was the variable, and the variable was with the programmer. From the simple statement to the complex condition, every line of code is a step toward creating a new world."

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiment   :** Fundamentals & Conditional Logic (Exp 1 & 2)  

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE VISION ✧
*The Objective*

To embark on a journey through the foundational syntax of Python, mastering the art of variable declaration, the precision of arithmetic operators, and the strategic branching of conditional logic.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE FOUNDATION ✧
*The Theory of Elements*

**The Basic Statement:**
Python is a language of elegance and power. It treats every piece of data as an object, dynamically inferring its nature (integer, float, string) with effortless grace. Through arithmetic and bitwise operators, we perform the alchemy of computation.

**The Conditional Decree:**
Logic is defined by choice. Using `if`, `elif`, and `else`, we guide our programs through the diverse paths of decision-making, ensuring that every condition met leads to a purposeful manifestation.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE BLUEPRINT ✧
*The Logic of the Canvas*

1.  **Initiation:** Verify the presence of the Python interpreter in the local environment.
2.  **Expression:** Declare variables and perform calculations using both standard operators and the `math` library's ancient wisdom.
3.  **Branching:** Implement multi-way decisions to solve puzzles involving divisibility, leap years, and academic grading.
4.  **Revelation:** Utilize the `print()` invocation to reveal the internal state of our logic to the user.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE CREATION ✧
*The Implementation of Logic*

### 1. The Alchemy of Variables & Operators
```python
import math

# --- 1. Geometric Resonance: Hypotenuse ---
def calculate_hypotenuse(a, b):
    """Manifests the diagonal length of a right triangle."""
    return math.sqrt(a**2 + b**2)

# --- 2. Temporal Conversion: Seconds to Time ---
def convert_seconds_to_time(total_seconds):
    """Transmutes raw seconds into hours, minutes, and seconds."""
    hours = total_seconds // 3600
    minutes = (total_seconds % 3600) // 60
    seconds = total_seconds % 60
    return f"{hours}h {minutes}m {seconds}s"

# --- 3. The Pythonic Swap ---
x, y = 5, 10
x, y = y, x  # An elegant exchange of values

# Manifestation
print(f"Hypotenuse: {calculate_hypotenuse(3, 4)} ✧")
print(f"Time Manifestation: {convert_seconds_to_time(3665)}")
```

### 2. The Architecture of Decision
```python
# --- 1. The Leap Year Oracle ---
def is_leap_year(year):
    """Determines if a year is a leap year through nested conditions."""
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return "Leap Year ✧"
    return "Standard Year"

# --- 2. The Academic Grade Sorter ---
def determine_grade(marks_list):
    """Sorts academic performance into defined grades."""
    average = sum(marks_list) / len(marks_list)
    cgpa = average / 10
    
    if cgpa >= 9.0: grade = "O"
    elif cgpa >= 8.0: grade = "A+"
    elif cgpa >= 7.0: grade = "A"
    elif cgpa >= 6.0: grade = "B+"
    else: grade = "F"
    
    return average, grade

# Manifestation
print(f"2024 Analysis: {is_leap_year(2024)}")
avg, grd = determine_grade([70, 80, 90, 60, 50])
print(f"Average: {avg}, Final Grade: {grd} ✧")
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE MANIFESTATION ✧
*The Output*

```text
Hypotenuse: 5.0 ✧
Time Manifestation: 1h 1m 5s
The Pythonic Swap: 10, 5 ✧

2024 Analysis: Leap Year ✧
Average: 70.0, Final Grade: A ✧
Roots of Equation: 2.0, 1.0
Greatest of Three: 8 ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE REFLECTION ✧
*The Conclusion*

Through these foundational experiments, I have mastered the basic syntax and conditional logic that form the backbone of Python programming. I have learned to appreciate the language's elegance, from its dynamic typing to its powerful control flow structures, setting a solid foundation for the complex creations yet to come.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈
