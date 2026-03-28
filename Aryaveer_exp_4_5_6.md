# ✧･ﾟ: *✧･ﾟ:* THE ARCHITECTURE OF DATA & LOGIC *:･ﾟ✧*:･ﾟ✧

```text
    ____        __         _____ __                     __                      
   / __ \____ _/ /_____ _ / ___// /________  _______  __/ /___  __________  _____
  / / / / __ `/ __/ __ `/ \__ \/ __/ ___/ / / / ___/ / / / __ \/ ___/ __ \/ ___/
 / /_/ / /_/ / /_/ /_/ / ___/ / /_/ /  / /_/ / /__  / / / /_/ / /  / /_/ (__  ) 
/_____/\__,_/\__/\__,_/ /____/\__/_/   \__,_/\___/ /_/_/\____/_/   \____/____/  
                                                                                
```

> "In the garden of computation, data is the seed, and logic is the water that brings it to life. To code is to compose a symphony of information."

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiments  :** 4, 5, & 6  

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ EXPERIMENT NO. 4: STRINGS & SETS ✧
*The Fabric of Text and the Purity of Collections*

### ✧ THE VISION ✧
*The Objective*

To delve into the intricate manipulation of strings and harness the mathematical elegance of sets, transforming raw sequences into meaningful insights and unique collections.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE FOUNDATION ✧
*The Theory of Elements*

**Strings: The Immutable Verse**
In Python, strings are more than mere characters; they are immutable sequences of Unicode, a tapestry that cannot be altered once woven. We navigate this tapestry through indexing and slicing, and transform its essence using methods like `upper()`, `split()`, and `join()`.

**Sets: The Sacred Circle**
A set is a collection of unique, unordered elements. It mirrors the mathematical ideal of a set, where duplicates are banished and operations like Union (`|`), Intersection (`&`), and Difference (`-`) allow us to compare and contrast collections with absolute precision.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

### ✧ THE BLUEPRINT ✧
*The Logic of the Canvas*

**Part A: The Capital Sentinel**
1.  Receive a string from the user's invocation.
2.  Traverse each character with a vigilant `for` loop.
3.  Identify uppercase letters using the `isupper()` oracle.
4.  Maintain a sacred count of these majestic characters.

**Part B: The Unique Lexicon**
1.  Gather a sentence of many words.
2.  Standardize the text to lowercase, removing the noise of case sensitivity.
3.  Dissolve the sentence into a list of words.
4.  Cast this list into a `set`, allowing the unique essence of each word to remain while duplicates fade away.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

### ✧ THE CREATION ✧
*The Implementation of Logic*

```python
# --- Program 1: The Upper Case Sentinel ---
def analyze_uppercase_majesty():
    """Analyzes a string to count the majestic uppercase characters."""
    text = input("Enter a string for majestic analysis: ")
    count = sum(1 for char in text if char.isupper())
    print(f"The tapestry contains {count} uppercase letters ✧")

# --- Program 2: The Alchemist's Unique Words ---
def manifest_unique_words():
    """Transforms a sentence into a set of unique, lowercase words."""
    sentence = input("\nEnter a sentence to find its unique essence: ")
    
    # Refining the words
    words = sentence.lower().split()
    unique_essence = set(words)
    
    print(f"Original Lexicon: {words}")
    print(f"Unique Essence: {unique_essence}")
    print(f"Total Unique Elements: {len(unique_essence)}")

if __name__ == "__main__":
    analyze_uppercase_majesty()
    manifest_unique_words()
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE MANIFESTATION ✧
*The Output*

```text
Enter a string for majestic analysis: Welcome to Python Programming Lab!
The tapestry contains 4 uppercase letters ✧

Enter a sentence to find its unique essence: Python is great and Python is easy to learn
Original Lexicon: ['python', 'is', 'great', 'and', 'python', 'is', 'easy', 'to', 'learn']
Unique Essence: {'python', 'is', 'great', 'and', 'easy', 'to', 'learn'}
Total Unique Elements: 7
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE REFLECTION ✧
*The Conclusion*

Through the study of Strings and Sets, I have learned to appreciate the balance between immutable sequences and unique collections. The ability to filter noise and extract the core essence of data is a fundamental skill in the art of programming.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ EXPERIMENT NO. 5: LISTS, TUPLES, & DICTIONARIES ✧
*The Containers of Complexity*

### ✧ THE VISION ✧
*The Objective*

To master the diverse vessels of Python's data structures—the mutable List, the immutable Tuple, and the associative Dictionary—understanding when to embrace change and when to preserve state.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE FOUNDATION ✧
*The Theory of Vessels*

**Lists (`[]`): The Fluid Collection**
Ordered and mutable, lists are the workhorses of data storage, allowing for growth, shrinkage, and transformation.

**Tuples (`()`): The Eternal Record**
Once defined, a tuple is a constant, offering safety and performance where data must remain untouched.

**Dictionaries (`{}`): The Map of Keys**
Associative arrays that link unique keys to values, providing a direct path to information with incredible efficiency.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

### ✧ THE BLUEPRINT ✧
*The Logic of the Canvas*

**Part A: The Runner-Up Search**
1.  Gather a collection of scores.
2.  Purify the list using a `set` to remove duplicate heights.
3.  Arrange the unique scores in descending order.
4.  Select the second element—the runner-up—from this refined list.

**Part B: The Digital Rolodex**
1.  Initialize a Dictionary as a repository for names and numbers.
2.  Allow the user to search this repository using a key (Name).
3.  Retrieve and reveal the associated value (Phone Number) if the key exists.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

### ✧ THE CREATION ✧
*The Implementation of Logic*

```python
# --- Program 1: The Runner-Up Score ---
def find_runner_up_glory():
    """Finds the second highest score among the participants."""
    print("--- The Quest for the Runner-Up ---")
    try:
        n = int(input("Enter number of participants: "))
        scores = list(map(int, input("Enter scores separated by space: ").split()))
        
        # Refining and sorting
        unique_scores = sorted(list(set(scores)), reverse=True)
        
        if len(unique_scores) > 1:
            print(f"The runner-up score is: {unique_scores[1]} ✧")
        else:
            print("The scores are too uniform to find a runner-up.")
    except ValueError:
        print("Invalid input. Please enter numbers only.")

# --- Program 2: The Contact Grimoire ---
def manage_contacts():
    """A dictionary-based lookup for contact information."""
    print("\n--- The Digital Contact Grimoire ---")
    contacts = {
        "Aryaveer": "9876543210",
        "Rahul": "8887776665",
        "Sneha": "7776665554"
    }
    
    query = input("Enter a name to summon their contact: ")
    number = contacts.get(query)
    
    if number:
        print(f"The number for {query} is: {number} ✧")
    else:
        print("This name is not inscribed in our grimoire.")

if __name__ == "__main__":
    find_runner_up_glory()
    manage_contacts()
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE MANIFESTATION ✧
*The Output*

```text
--- The Quest for the Runner-Up ---
Enter number of participants: 5
Enter scores separated by space: 23 45 45 12 30
The runner-up score is: 30 ✧

--- The Digital Contact Grimoire ---
Enter a name to summon their contact: Aryaveer
The number for Aryaveer is: 9876543210 ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE REFLECTION ✧
*The Conclusion*

The choice of a data structure is the first brushstroke of a programmer's masterpiece. I have learned that while lists offer versatility, dictionaries offer the speed and clarity required for complex data management.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ EXPERIMENT NO. 6: THE ART OF FUNCTIONS ✧
*Modular Logic and Elegant Abstractions*

### ✧ THE VISION ✧
*The Objective*

To explore the modular nature of Python through user-defined functions, the recursive echoes of logic, and the concise power of anonymous Lambda functions.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE FOUNDATION ✧
*The Theory of Abstraction*

**The Function: A Reusable Verse**
Functions are the building blocks of modularity, allowing us to define a logic once and invoke it infinitely.

**Recursion: The Echoing Logic**
A function that calls itself, recursion is a powerful tool for solving problems that contain smaller versions of themselves, like the Fibonacci sequence.

**Lambda: The Anonymous Spark**
Short, one-line functions that provide a concise way to define mathematical or logical operations on the fly.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

### ✧ THE BLUEPRINT ✧
*The Logic of the Canvas*

**Part A: The Recursive Fibonacci**
1.  Define a base case: `n=0` or `n=1`.
2.  Define the recursive step: `f(n) = f(n-1) + f(n-2)`.
3.  Invoke the function iteratively to manifest the sequence.

**Part B: The Geometric Lambda**
1.  Craft a Lambda function for the volume of a cone: `V = (1/3)πr²h`.
2.  Invoke this anonymous spark with user-provided dimensions.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

### ✧ THE CREATION ✧
*The Implementation of Logic*

```python
import math

# --- The Recursive Echo ---
def fibonacci_recursive(n):
    """Calculates the n-th Fibonacci term through recursive echoes."""
    if n <= 1:
        return n
    return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)

# --- The Lambda Spark ---
# Geometric Volume of a Cone: (1/3) * pi * r^2 * h
calculate_cone_volume = lambda r, h: (1/3) * math.pi * (r**2) * h

def main_orchestration():
    """Orchestrates the demonstration of functions."""
    # 1. Manifesting the Fibonacci Sequence
    print("--- The Fibonacci Manifestation ---")
    try:
        limit = int(input("How many terms shall we manifest? "))
        print("Sequence:", end=" ")
        for i in range(limit):
            print(fibonacci_recursive(i), end=" ")
        print()
    except ValueError:
        print("Please enter a valid integer.")

    # 2. Calculating Geometric Volume
    print("\n--- The Geometric Lambda ---")
    try:
        radius = float(input("Enter the radius of the cone: "))
        height = float(input("Enter the height of the cone: "))
        volume = calculate_cone_volume(radius, height)
        print(f"The Volume of the cone is: {volume:.4f} ✧")
    except ValueError:
        print("Invalid dimensions provided.")

if __name__ == "__main__":
    main_orchestration()
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE MANIFESTATION ✧
*The Output*

```text
--- The Fibonacci Manifestation ---
How many terms shall we manifest? 10
Sequence: 0 1 1 2 3 5 8 13 21 34 

--- The Geometric Lambda ---
Enter the radius of the cone: 5
Enter the height of the cone: 7
The Volume of the cone is: 183.2596 ✧
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

### ✧ THE REFLECTION ✧
*The Conclusion*

Modular programming is the bridge between complexity and clarity. Through functions and recursion, I have learned to decompose large problems into elegant, manageable pieces. Lambda functions have taught me the beauty of brevity in logic.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈
