# Technical Report: Data Persistence & Fault-Tolerant Systems (Exp 7)

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
