# Lab Report: Python Programming

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiment   :** Loops in Python (Experiment 3)  

---

## Experiment No. 3: Control Flow with Loops

### 1. Aim
To study and implement various looping statements (for and while) in Python for solving mathematical and logical problems.

### 2. Theory
Loops are used in programming to repeat a specific block of code multiple times. Python provides two primary types of loops:
- **`for` loop:** Typically used when the number of iterations is known in advance. It iterates over a sequence (list, tuple, string) or a range.
- **`while` loop:** Used to execute a block of code as long as a specified condition remains true. It is ideal for situations where the number of iterations is not predetermined.

Key control statements like `break` (to exit the loop) and `continue` (to skip the current iteration) are often used to manage loop execution flow.

### 3. Algorithm / Steps
1.  **Input:** Obtain necessary values from the user using `input()`.
2.  **Initialization:** Set up initial variables (like counters or accumulators).
3.  **Looping Logic:**
    -   Use `for` with `range()` for fixed iterations.
    -   Use `while` with a condition for dynamic iterations.
    -   Perform calculations or checks inside the loop body.
4.  **Termination:** Ensure the loop has a clear exit condition to avoid infinite execution.
5.  **Output:** Display the final result using `print()`.

### 4. Program Code

#### 1. Factorial of a Number
```python
n = int(input("Enter a number: "))
fact = 1
for i in range(1, n + 1):
    fact *= i
print("Factorial =", fact)
```

#### 2. Armstrong Number Check
```python
num = int(input("Enter a number: "))
temp = num
total = 0
while temp > 0:
    digit = temp % 10
    total += digit ** 3
    temp //= 10
if total == num:
    print("Armstrong Number")
else:
    print("Not an Armstrong Number")
```

#### 3. Fibonacci Series
```python
n = int(input("Enter number of terms: "))
a, b = 0, 1
for i in range(n):
    print(a, end=" ")
    a, b = b, a + b
```

#### 4. Prime Number Check
```python
num = int(input("Enter a number: "))
if num > 1:
    for i in range(2, num):
        if num % i == 0:
            print(num, "is not a Prime Number")
            break
    else:
        print(num, "is a Prime Number")
else:
    print(num, "is not a Prime Number")
```

#### 5. Palindrome Number
```python
num = int(input("Enter a number: "))
temp = num
rev = 0
while temp > 0:
    rev = rev * 10 + temp % 10
    temp //= 10
if rev == num:
    print("Palindrome Number")
else:
    print("Not a Palindrome")
```

#### 6. Sum of Digits
```python
num = int(input("Enter a number: "))
total = 0
temp = num
while temp > 0:
    total += temp % 10
    temp //= 10
print("Sum of digits =", total)
```

#### 7. Numbers Divisible by 5 or 7 (1 to 100)
```python
count = 0
for i in range(1, 101):
    if i % 5 == 0 or i % 7 == 0:
        print(i, end=" ")
        count += 1
print("\nCount =", count)
```

#### 8. String Case Conversion (Lowercase to Uppercase)
```python
text = input("Enter a string: ")
result = ""
for ch in text:
    result += ch.upper()
print("Uppercase:", result)
```

#### 9. Multiplication Table
```python
num = int(input("Enter a number: "))
for i in range(1, 11):
    print(num, "*", i, "=", num * i)
```

#### 10. Pattern Printing
```python
for i in range(5, 0, -1):
    for j in range(1, i + 1):
        print(j, end="")
    for k in range(6 - i):
        print("*", end="")
    for k in range(5 - i):
        print("*", end="")
    for j in range(i, 0, -1):
        print(j, end="")
    print()
```

#### 11. Sum of Harmonic Series (1/n)
```python
n = int(input("Enter value of n: "))
series_sum = 0.0
for i in range(1, n + 1):
    series_sum += 1 / i
print("Sum of series =", series_sum)
```

### 5. Explanation of the Code
- **Factorial:** Uses a `for` loop to multiply a sequence of numbers from 1 to `n`.
- **Armstrong:** Calculates the sum of cubes of each digit using a `while` loop and compares it with the original number.
- **Fibonacci:** Employs tuple unpacking `a, b = b, a + b` to update sequence terms efficiently.
- **Prime Check:** Uses a `for-else` block where the `else` executes only if the loop finishes without hitting a `break`.
- **Palindrome:** Reverses the integer mathematically using modulo and floor division.
- **Pattern:** Nested loops manage both the numeric sequences and the star decorations for each row.

### 6. Output

```bash
PS C:\Users\lohia> python factorial.py
Enter a number: 5
Factorial = 120

PS C:\Users\lohia> python armstrong.py
Enter a number: 153
Armstrong Number

PS C:\Users\lohia> python fibonacci.py
Enter number of terms: 6
0 1 1 2 3 5 

PS C:\Users\lohia> python prime.py
Enter a number: 17
17 is a Prime Number

PS C:\Users\lohia> python palindrome.py
Enter a number: 121
Palindrome Number

PS C:\Users\lohia> python sum_digits.py
Enter a number: 456
Sum of digits = 15

PS C:\Users\lohia> python div_check.py
5 7 10 14 15 20 21 25 28 30 35 40 42 45 49 50 55 56 60 63 65 70 75 77 80 84 85 90 91 95 98 100 
Count = 32

PS C:\Users\lohia> python convert.py
Enter a string: python lab
Uppercase: PYTHON LAB

PS C:\Users\lohia> python table.py
Enter a number: 7
7 * 1 = 7
7 * 2 = 14
7 * 3 = 21
...
7 * 10 = 70

PS C:\Users\lohia> python pattern.py
123451
1234***4321
123*****321
12*******21
1*********1

PS C:\Users\lohia> python harmonic.py
Enter value of n: 5
Sum of series = 2.283333333333333
```

### 7. Result / Conclusion
All looping programs were successfully implemented and tested. I have gained a deep understanding of how `for` and `while` loops can be applied to solve diverse mathematical sequences and logic-based problems in Python.
