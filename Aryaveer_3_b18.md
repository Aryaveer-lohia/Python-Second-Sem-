# ✧･ﾟ: *✧･ﾟ:* THE ART OF ITERATION *:･ﾟ✧*:･ﾟ✧

```text
      _____                                                   
     /  _  \_______ ___.__. _____ ___  __ ____   ___________ 
    /  /_\  \_  __ <   |  | \__  \\  \/ // __ \_/ __ \_  __ \
   /    |    \  | \/\___  |  / __ \\   /\  ___/\  ___/|  | \/
   \____|__  /__|   / ____| (____  /\_/  \___  >\___  >__|   
           \/       \/           \/          \/     \/       
```

> "Programming is not just about telling a computer what to do; it is the art of expressing elegant logic through the canvas of code."

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiment   :** Loops in Python (Experiment 3)  

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE VISION ✧
*The Objective*

To explore and master the rhythmic dance of control flow through the implementation of `for` and `while` loops in Python, transforming mathematical challenges into logical symphonies.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE FOUNDATION ✧
*The Theory of Cycles*

In the realm of Python, loops are the mechanisms of repetition, allowing a single breath of code to echo across multiple iterations.

*   **The `for` Loop:** A structured traversal, ideal for navigating sequences (lists, tuples, strings) or predefined ranges where the journey's length is known.
*   **The `while` Loop:** A conditional vigil, continuing its execution as long as the truth of its predicate remains steadfast.

With the guidance of `break` and `continue`, we gain the power to interrupt or skip steps within these cycles, ensuring our logic remains as precise as it is powerful.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE BLUEPRINT ✧
*The Logic of the Canvas*

1.  **Invocation:** Gather the necessary elements from the user through the `input()` function.
2.  **Preparation:** Initialize the sacred variables—counters, accumulators, and flags.
3.  **The Iterative Dance:**
    -   Employ `for` with `range()` for journeys of a fixed distance.
    -   Invoke `while` for paths dictated by a shifting condition.
    -   Execute the core transformation or calculation within the loop's embrace.
4.  **Graceful Exit:** Define clear boundaries to prevent the loop from descending into the chaos of infinity.
5.  **Revelation:** Present the final manifestation of logic using `print()`.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE CREATION ✧
*The Implementation of Logic*

### 1. The Symphony of Factorials
```python
# Calculating the factorial of a number
try:
    n = int(input("Enter a number to find its factorial: "))
    factorial = 1
    
    # Multiplying through the range
    for i in range(1, n + 1):
        factorial *= i
        
    print(f"The Factorial of {n} is: {factorial}")
except ValueError:
    print("Invalid input! Please enter an integer.")
```

### 2. The Quest for Armstrong Numbers
```python
# Verifying if a number is an Armstrong number
num = int(input("Enter a number to check: "))
temp = num
total = 0

# Extracting and cubing digits
while temp > 0:
    digit = temp % 10
    total += digit ** 3
    temp //= 10

if total == num:
    print(f"{num} is an Armstrong Number ✧")
else:
    print(f"{num} is not an Armstrong Number")
```

### 3. The Fibonacci Sequence
```python
# Weaving the Fibonacci series
n = int(input("Enter the number of terms to manifest: "))
a, b = 0, 1

print("Fibonacci Series:", end=" ")
for _ in range(n):
    print(a, end=" ")
    a, b = b, a + b
print()
```

### 4. The Prime Sentinel
```python
# Determining the purity of a Prime number
num = int(input("Enter a number for the prime check: "))

if num > 1:
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            print(f"{num} is not a Prime Number.")
            break
    else:
        print(f"{num} is a Prime Number ✧")
else:
    print(f"{num} is not a Prime Number.")
```

### 5. The Mirror of Palindromes
```python
# Checking for numeric symmetry
num = int(input("Enter a number to mirror: "))
temp = num
reverse_num = 0

while temp > 0:
    reverse_num = (reverse_num * 10) + (temp % 10)
    temp //= 10

if reverse_num == num:
    print(f"{num} is a Palindrome ✧")
else:
    print(f"{num} is not a Palindrome.")
```

### 6. The Harmony of Digits
```python
# Summing the essence of digits
num = int(input("Enter a number to sum its digits: "))
total_sum = 0
temp = num

while temp > 0:
    total_sum += temp % 10
    temp //= 10

print(f"The sum of digits is: {total_sum}")
```

### 7. The Selective Divisors
```python
# Finding numbers aligned with 5 or 7
print("Manifesting numbers divisible by 5 or 7 (1-100):")
count = 0
for i in range(1, 101):
    if i % 5 == 0 or i % 7 == 0:
        print(i, end=" ")
        count += 1
print(f"\nTotal count: {count}")
```

### 8. The Alchemist's Case Conversion
```python
# Transforming lowercase whispers into uppercase echoes
text = input("Enter a string to transform: ")
print(f"Manifestation: {text.upper()}")
```

### 9. The Grid of Multiplications
```python
# Building the table of multiples
num = int(input("Enter a number for its multiplication table: "))
print(f"--- Table of {num} ---")
for i in range(1, 11):
    print(f"{num} x {i} = {num * i}")
```

### 10. The Geometric Pattern
```python
# Sculpting a pattern from numbers and stars
for i in range(5, 0, -1):
    # Ascending numbers
    for j in range(1, i + 1):
        print(j, end="")
    # The starry void
    print("*" * (10 - 2 * i), end="")
    # Descending numbers
    for j in range(i, 0, -1):
        print(j, end="")
    print()
```

### 11. The Harmonic Resonance
```python
# Summing the harmonic series
n = int(input("Enter value of n for the harmonic series: "))
harmonic_sum = sum(1/i for i in range(1, n + 1))
print(f"The Harmonic Sum is: {harmonic_sum:.4f}")
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE MANIFESTATION ✧
*The Output*

```text
Enter a number to find its factorial: 5
The Factorial of 5 is: 120

Enter a number to check: 153
153 is an Armstrong Number ✧

Enter the number of terms to manifest: 6
Fibonacci Series: 0 1 1 2 3 5 

Enter a number for its multiplication table: 7
--- Table of 7 ---
7 x 1 = 7
7 x 2 = 14
...
7 x 10 = 70

123451
1234**4321
123****321
12******21
1********1
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE REFLECTION ✧
*The Conclusion*

Through this journey of logic and artistry, I have mastered the rhythmic pulse of loops in Python. Whether navigating the predictable path of a `for` loop or the dynamic waters of a `while` loop, I have learned to craft code that is both functional and elegant, solving mathematical puzzles with the grace of a digital artist.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈
