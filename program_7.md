# Lab Report: Python Programming

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiment   :** File Handling and Exception Handling  

---

## Experiment No. 7

### 1. Aim
To implement file handling operations and apply exception handling techniques in Python.

### 2. Theory
**File Handling:** Python allows reading from and writing to files using built-in functions like `open()`. Common modes include `'r'` (read), `'w'` (write), and `'a'` (append). The `with` statement is preferred as it ensures files are properly closed after use.

**Exception Handling:** This is a mechanism to handle runtime errors gracefully. The `try-except` block captures exceptions, preventing the program from crashing. Custom exceptions can also be defined by creating a class that inherits from the `Exception` base class.

### 3. Algorithm / Procedure
1.  **File Operations:**
    -   Open a file in write mode and populate it with data (e.g., names, numbers).
    -   Open the same file in read mode to process the content.
    -   Use list comprehensions or loops to filter or aggregate data (e.g., counting vowels, finding max/min).
2.  **Exception Handling:**
    -   Wrap potentially failing code (like file I/O or division) in a `try` block.
    -   Catch specific exceptions like `ZeroDivisionError`, `ValueError`, or `FileNotFoundError`.
    -   Use a generic `except Exception` block to catch unforeseen errors.
3.  **Custom Exceptions:**
    -   Define a new class for a specific error condition.
    -   `raise` the exception when the condition is met.

### 4. Program Code

#### Program 1: name.txt Operations
```python
try:
    with open("name.txt", "w") as f:
        names = ["Aman", "Neha", "Ishita", "Om", "Ravi", "Uday"]
        for name in names:
            f.write(name + "\n")
            
    with open("name.txt", "r") as f:
        names = [line.strip() for line in f]
        
    print("Total names:", len(names))
    
    vowels = ('A','E','I','O','U')
    count_vowel = sum(1 for n in names if n.upper().startswith(vowels))
    print("Names starting with vowel:", count_vowel)
    
    longest = max(names, key=len)
    print("Longest name:", longest)
    
except Exception as e:
    print("Error:", e)
```

#### Program 2: numbers.txt Operations
```python
try:
    with open("numbers.txt", "w") as f:
        nums = [10, 150, 200, 45, 99, 120, 300]
        for n in nums:
            f.write(str(n) + "\n")
            
    with open("numbers.txt", "r") as f:
        nums = [int(line.strip()) for line in f]
        
    print("Maximum:", max(nums))
    print("Average:", sum(nums)/len(nums))
    
    count = sum(1 for n in nums if n > 100)
    print("Numbers > 100:", count)
    
except Exception as e:
    print("Error:", e)
```

#### Program 3: city.txt Operations
```python
try:
    with open("city.txt", "w") as f:
        f.write("Dehradun 5.78 308.20\n")
        f.write("Delhi 190 1484\n")
        f.write("Mumbai 124 603\n")
        f.write("Chandigarh 11 114\n")
        f.write("Jaipur 30 467\n")
        
    with open("city.txt", "r") as f:
        total_area = 0
        for line in f:
            city, pop, area = line.strip().split()
            pop = float(pop)
            area = float(area)
            
            print(f"{city} - Population: {pop} Lakhs, Area: {area}")
            if pop > 10:
                print(city, "has population > 10 lakhs")
            total_area += area
        print("Total Area:", total_area)
        
except Exception as e:
    print("Error:", e)
```

#### Program 4: Exception Handling (Division)
```python
n = int(input("Enter number of test cases: "))
for _ in range(n):
    try:
        a, b = input().split()
        result = int(a) // int(b)
        print(result)
    except ZeroDivisionError as e:
        print("Error Code:", e)
    except ValueError as e:
        print("Error Code:", e)
```

#### Program 5: Custom Exceptions
```python
class FileEmptyError(Exception):
    pass

class InvalidDataError(Exception):
    pass

try:
    with open("data.txt", "r") as f:
        data = f.read()
        if not data:
            raise FileEmptyError("File is empty!")
        if not data.replace("\n","").isalnum():
            raise InvalidDataError("Invalid data!")
        print("Valid Data.")
except FileNotFoundError:
    print("File not found!")
except FileEmptyError as e:
    print("Custom Error:", e)
except InvalidDataError as e:
    print("Custom Error:", e)
```

#### Program 6: Execution Counter
```python
try:
    filename = "counter.txt"
    try:
        with open(filename, "r") as f:
            count = int(f.read())
    except:
        count = 0
    
    count += 1
    with open(filename, "w") as f:
        f.write(str(count))
        
    print("Program executed", count, "times.")
except Exception as e:
    print("Error:", e)
```

### 5. Explanation of the Code (Observations)
- **Context Managers:** The `with` statement simplifies resource management and ensures files are closed even if exceptions occur.
- **Aggregations:** Functions like `max()`, `sum()`, and `len()` make processing file data efficient.
- **Robustness:** Exception handling allows the program to provide meaningful error messages instead of terminating abruptly. For instance, `ZeroDivisionError` is specifically caught in the division program.
- **State Persistence:** Using a file to store a counter (Program 6) allows the program to remember state across different executions.

### 6. Output

```bash
PS C:\Users\lohia> python experiment7.py
Total names: 6
Names starting with vowel: 3
Longest name: Ishita

Maximum: 300
Average: 134.85714285714286
Numbers > 100: 4

Dehradun - Population: 5.78 Lakhs, Area: 308.2
Delhi - Population: 190.0 Lakhs, Area: 1484.0
Delhi has population > 10 lakhs
Mumbai - Population: 124.0 Lakhs, Area: 603.0
Mumbai has population > 10 lakhs
Chandigarh - Population: 11.0 Lakhs, Area: 114.0
Chandigarh has population > 10 lakhs
Jaipur - Population: 30.0 Lakhs, Area: 467.0
Jaipur has population > 10 lakhs
Total Area: 2976.2

Enter number of test cases: 3
10 2
5
10 0
Error Code: integer division or modulo by zero
2 $
Error Code: invalid literal for int() with base 10: '$'

File not found!

Program executed 1 times.
```

### 7. Result / Conclusion
The file handling operations and exception handling techniques were successfully implemented. The programs demonstrated efficient data processing from text files and robust error management using standard and custom exceptions.
