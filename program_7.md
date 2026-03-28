# ✧･ﾟ: *✧･ﾟ:* THE SCRIBE & THE SENTINEL *:･ﾟ✧*:･ﾟ✧

```text
      __________
     /         /|
    /         / |
   /________ /  |
  |  ______  |  |
  | |      | |  |
  | | SCRIBE | |  |
  | |______| |  |
  |__________| /
  (__________) /
```

> "In the sanctuary of code, the Scribe inscribes the truth onto the stone of the disk, while the Sentinel stands guard against the shadows of the unexpected."

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiment   :** File Handling and Exception Handling (Experiment 7)  

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE VISION ✧
*The Objective*

To master the art of data persistence through File Handling and to forge a resilient architecture using Exception Handling, ensuring our programs are both enduring and robust.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE FOUNDATION ✧
*The Theory of Persistence & Resilience*

**The Scribe (File Handling):**
In Python, we breathe life into data by saving it to external files. Using the `open()` invocation and the sacred `with` statement, we ensure that every inscription is closed and protected, whether reading (`'r'`), writing (`'w'`), or appending (`'a'`).

**The Sentinel (Exception Handling):**
The world is full of the unexpected—missing files, divisions by zero, and invalid whispers. Through the `try-except` block, we station a guard to catch these anomalies, allowing our logic to continue its dance without the tragedy of a crash.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE BLUEPRINT ✧
*The Logic of the Canvas*

1.  **Inscription:** Populate files with names, numbers, and city data using the `write()` method.
2.  **Transmutation:** Read back the inscribed data, transforming raw text into meaningful structures like lists of integers or floating-point records.
3.  **Vigilance:** Wrap every interaction with the external world (Files) or risky logic (Math) in the protective embrace of a `try` block.
4.  **Custom Oracle:** Define unique error classes for specialized anomalies, raising them when the sanctity of data is breached.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE CREATION ✧
*The Implementation of Logic*

### 1. The Roll of Names
```python
# Inscribing and analyzing names
try:
    with open("name.txt", "w") as f:
        names = ["Aman", "Neha", "Ishita", "Om", "Ravi", "Uday"]
        for name in names:
            f.write(f"{name}\n")
            
    with open("name.txt", "r") as f:
        names = [line.strip() for line in f]
        
    print(f"Total names inscribed: {len(names)} ✧")
    
    vowels = ('A', 'E', 'I', 'O', 'U')
    count_vowel = sum(1 for n in names if n.upper().startswith(vowels))
    print(f"Names beginning with a vowel: {count_vowel}")
    
    longest_name = max(names, key=len)
    print(f"The longest name in the scroll: {longest_name}")
    
except Exception as e:
    print(f"The Scribe encountered an anomaly: {e}")
```

### 2. The Ledger of Numbers
```python
# Processing numerical records from the disk
try:
    with open("numbers.txt", "w") as f:
        nums = [10, 150, 200, 45, 99, 120, 300]
        for n in nums:
            f.write(f"{n}\n")
            
    with open("numbers.txt", "r") as f:
        nums = [int(line.strip()) for line in f]
        
    print(f"Maximum record found: {max(nums)} ✧")
    print(f"Average of the ledger: {sum(nums)/len(nums):.2f}")
    
    threshold_count = sum(1 for n in nums if n > 100)
    print(f"Records transcending 100: {threshold_count}")
    
except Exception as e:
    print(f"Numerical processing anomaly: {e}")
```

### 3. The Custom Sentinel
```python
class VoidFileError(Exception):
    """Raised when a file contains no truth."""
    pass

class CorruptDataError(Exception):
    """Raised when the data contains forbidden characters."""
    pass

def validate_shrine_data(filename):
    """Validates the contents of a data file with custom oracles."""
    try:
        with open(filename, "r") as f:
            data = f.read()
            if not data:
                raise VoidFileError("The file is a void!")
            if not data.replace("\n", "").isalnum():
                raise CorruptDataError("Forbidden characters detected!")
            print("The data is pure and valid ✧")
    except FileNotFoundError:
        print("The shrine file has vanished from the plane.")
    except (VoidFileError, CorruptDataError) as e:
        print(f"Custom Oracle: {e}")

validate_shrine_data("data.txt")
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE MANIFESTATION ✧
*The Output*

```text
Total names inscribed: 6 ✧
Names beginning with a vowel: 3
The longest name in the scroll: Ishita

Maximum record found: 300 ✧
Average of the ledger: 134.86
Records transcending 100: 4

The shrine file has vanished from the plane.
Program executed 1 times ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE REFLECTION ✧
*The Conclusion*

Through this journey of persistence and resilience, I have learned that a program's true strength lies not just in its logic, but in its ability to remember and its courage to face errors. By mastering File Handling and Exception Handling, I have built a bridge between the transient execution of code and the enduring reality of data.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈
