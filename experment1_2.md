# Lab Report: Python Programming

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiment   :** Python Installation, Basic Statements, and Conditional Statements  

---

## Experiment No. 1 & 2

### 1. Aim
- **Experiment 1:** To understand Python installation, basic syntax, variables, operators, and simple programs.
- **Experiment 2:** To understand decision-making using conditional statements in Python.

### 2. Theory
Python is a high-level, interpreted programming language known for its simplicity and readability. It supports multiple programming paradigms, including procedural, object-oriented, and functional programming. 

**Basic Statements:** Python uses variables to store data, and operators (arithmetic, comparison, logical, bitwise, etc.) to perform operations on them. The `print()` function is used to output data to the console.

**Conditional Statements:** These are used to execute a block of code only if a specified condition is met. The `if`, `elif`, and `else` keywords are used for decision-making logic.

### 3. Algorithm / Procedure
1.  **Installation:** Verify Python installation using `python --version`.
2.  **Basic Operations:**
    -   Define variables of different types (int, float, string, boolean).
    -   Use arithmetic operators for calculations.
    -   Use math library functions (e.g., `sqrt`) for complex calculations.
    -   Apply bitwise and membership operators.
3.  **Conditional Logic:**
    -   Take input or define values.
    -   Use `if-elif-else` structures to check conditions (e.g., divisibility, comparison, grading).
    -   Display appropriate results based on the evaluated conditions.

### 4. Program Code

#### Experiment 1: Basic Python Statements

```python
# 1. Print Age and Its Data Type
age = 21
print(age)
print(type(age))

# 2. String Variable
x = "Hello"
print(x)

# 3. Printing Different Data Types
a = 10
b = 3.14
c = "Python"
d = True
print(a, b, c, d)

# 4. Arithmetic Operations
x = 9
y = 7
print("Addition:", x + y)
print("Multiplication:", x * y)
print("Division:", x / y)
print("Subtraction:", x - y)

# 5. Hypotenuse Using Pythagoras Theorem
import math
a = 3
b = 4
c = math.sqrt(a*a + b*b)
print("Hypotenuse:", c)

# 6. Simple Interest
p = 1000
r = 5
t = 2
si = (p * r * t) / 100
print("Simple Interest:", si)

# 7. Area of Triangle
import math
a = 3
b = 4
c = 5
s = (a + b + c) / 2
area = math.sqrt(s*(s-a)*(s-b)*(s-c))
print("Area:", area)

# 8. Convert Seconds
seconds = 3665
hours = seconds // 3600
seconds %= 3600
minutes = seconds // 60
seconds %= 60
print(hours, "hours", minutes, "minutes", seconds, "seconds")

# 9. Swap Two Numbers
a = 5
b = 10
a, b = b, a
print(a, b)

# 10. Sum of First n Natural Numbers
n = 10
sum = n * (n + 1) // 2
print("Sum:", sum)

# 11. Bitwise Operators
a = 1
b = 0
print("AND:", a & b)
print("OR:", a | b)
print("XOR:", a ^ b)

# 12. Shift Operators
x = 8
print("Left Shift:", x << 1)
print("Right Shift:", x >> 1)

# 13. Membership Operator
seq = (10, 20, 56, 78, 89)
num = 56
print(num in seq)
```

#### Experiment 2: Conditional Statements

```python
# 1. Divisible by 3 and 5
num = 15
if num % 3 == 0 and num % 5 == 0:
    print("Divisible by 3 and 5")
else:
    print("Not divisible")

# 2. Multiple of Five
num = 25
if num % 5 == 0:
    print("Multiple of five")
else:
    print("Not a multiple")

# 3. Greatest of Two Numbers
a = 10
b = 10
if a > b:
    print("a is greater")
elif b > a:
    print("b is greater")
else:
    print("numbers are equal")

# 4. Greatest of Three Numbers
a, b, c = 5, 8, 3
if a > b and a > c:
    print("a is greatest")
elif b > c:
    print("b is greatest")
else:
    print("c is greatest")

# 5. Quadratic Equation
import math
a, b, c = 1, -3, 2
d = b*b - 4*a*c
if d > 0:
    r1 = (-b + math.sqrt(d)) / (2*a)
    r2 = (-b - math.sqrt(d)) / (2*a)
    print(r1, r2)
elif d == 0:
    r = -b / (2*a)
    print(r)
else:
    print("Imaginary roots")

# 6. Leap Year
year = 2024
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print("Leap Year")
else:
    print("Not a Leap Year")

# 7. Next Date
day = 20
month = 9
year = 2005
day += 1
print(day, month, year)

# 8. Grade Sheet
marks = [70, 80, 90, 60, 50]
total = sum(marks)
percentage = total / 5
cgpa = percentage / 10
if cgpa <= 3.4:
    grade = "F"
elif cgpa <= 5.0:
    grade = "C+"
elif cgpa <= 6.0:
    grade = "B"
elif cgpa <= 7.0:
    grade = "B+"
elif cgpa <= 8.0:
    grade = "A"
elif cgpa <= 9.0:
    grade = "A+"
else:
    grade = "O"
print("Percentage:", percentage)
print("CGPA:", cgpa)
print("Grade:", grade)
```

### 5. Explanation of the Code (Observations)
- **Data Types:** Python dynamically infers the type of a variable based on the assigned value.
- **Arithmetic & Logic:** Operations follow standard mathematical precedence. Math module provides advanced functions.
- **Swapping:** Python allows simultaneous assignment `a, b = b, a`, which is an elegant way to swap values without a temporary variable.
- **Control Flow:** `if-elif-else` blocks handle multi-way branching effectively. Logical operators `and` / `or` combine conditions.

### 6. Output

```bash
PS C:\Users\lohia> python experiment1.py
21
<class 'int'>
Hello
10 3.14 Python True
Addition: 16
Multiplication: 63
Division: 1.2857142857142858
Subtraction: 2
Hypotenuse: 5.0
Simple Interest: 100.0
Area: 6.0
1 hours 1 minutes 5 seconds
10 5
Sum: 55
AND: 0
OR: 1
XOR: 1
Left Shift: 16
Right Shift: 4
True

PS C:\Users\lohia> python experiment2.py
Divisible by 3 and 5
Multiple of five
numbers are equal
b is greatest
2.0 1.0
Leap Year
21 9 2005
Percentage: 70.0
CGPA: 7.0
Grade: B+
```

### 7. Result / Conclusion
All programs for Experiments 1 and 2 were executed successfully. The basic syntax, operators, and conditional statements of Python were thoroughly understood and verified through various practical examples.
