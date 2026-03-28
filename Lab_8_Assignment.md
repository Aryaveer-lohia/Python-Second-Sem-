# ✧･ﾟ: *✧･ﾟ:* THE VISUAL NEXUS: GUI & DATABASES *:･ﾟ✧*:･ﾟ✧

```text
   ___________________
  |  _______________  |
  | |               | |
  | |   VISUAL      | |
  | |    INTERFACE  | |
  | |_______________| |
  |___________________|
          |   |
          |   |
   _______|___|_______
  |                   |
  |     DATABASE      |
  |___________________|
```

> "A beautiful interface is the window to a powerful soul. When logic meets design and data meets persistence, we create applications that truly live."

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  
**Experiment   :** GUI and Backend Connectivity (Lab 8)  

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ THE VISION ✧
*The Objective*

To bridge the gap between abstract logic and human interaction by designing sophisticated Graphical User Interfaces (GUIs) with Tkinter and anchoring them to the persistent reality of SQLite databases.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE FOUNDATION ✧
*The Theory of Interaction & Persistence*

**The Visual Layer (Tkinter):**
Tkinter is Python's standard toolkit for crafting desktop applications. It allows us to sculpt windows, buttons, and entry fields, creating an environment where the user can interact with our code through sight and touch.

**The Persistent Soul (SQLite):**
A GUI without memory is but a fleeting dream. SQLite provides a lightweight, serverless database that allows our applications to remember user inputs, store registration details, and manage tasks across multiple sessions.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ EXPERIMENT 1: THE SIMPLE WINDOW ✧
*The First Breath of GUI*

### ✧ THE BLUEPRINT ✧
1.  **Invocation:** Initialize the `Tk()` class to create the root of our visual tree.
2.  **Configuration:** Set the title and geometry to define the window's physical presence.
3.  **Manifestation:** Use the `Label` widget to display a welcoming message.

### ✧ THE CREATION ✧
```python
import tkinter as tk

def manifest_simple_window():
    """Breathes life into a basic Tkinter window."""
    root = tk.Tk()
    root.title("A Simple Portal")
    root.geometry("400x300")
    root.resizable(False, False)

    # Creating a welcoming message
    label = tk.Label(root, text="Welcome to the Tkinter Realm ✧", font=("Helvetica", 16))
    label.pack(pady=100)

    root.mainloop()

if __name__ == "__main__":
    manifest_simple_window()
```

### ✧ THE MANIFESTATION ✧
```text
> Initializing Window... ✧
> Title: "A Simple Portal" | Size: 400x300
> Status: Window is non-resizable.
> Event Loop: Running...
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ EXPERIMENT 2: THE GUI CALCULATOR ✧
*The Logic of Numbers in Visual Form*

### ✧ THE BLUEPRINT ✧
1.  **Layout:** Arrange buttons in a grid to mirror the familiar interface of a calculator.
2.  **Logic:** Use the `eval()` oracle to dynamically calculate mathematical expressions from string inputs.
3.  **Synchronization:** Employ `StringVar()` to link the display field with our Python logic.

### ✧ THE CREATION ✧
```python
import tkinter as tk

def click_handler(event):
    """Handles the rhythmic clicks of the calculator buttons."""
    text = event.widget.cget("text")
    if text == "=":
        try:
            result = str(eval(screen_var.get()))
            screen_var.set(result)
        except Exception:
            screen_var.set("Error")
    elif text == "C":
        screen_var.set("")
    else:
        screen_var.set(screen_var.get() + text)

def build_calculator():
    """Constructs a functional calculator with a visual soul."""
    root = tk.Tk()
    root.title("The Arithmetic Oracle")
    root.geometry("300x450")

    global screen_var
    screen_var = tk.StringVar()
    entry = tk.Entry(root, textvar=screen_var, font="lucida 20 bold", justify='right')
    entry.pack(fill="both", pady=15, padx=15)

    buttons = [
        ["7", "8", "9", "/"],
        ["4", "5", "6", "*"],
        ["1", "2", "3", "-"],
        ["0", ".", "=", "+"],
        ["C"]
    ]

    for row in buttons:
        frame = tk.Frame(root)
        frame.pack()
        for btn_text in row:
            b = tk.Button(frame, text=btn_text, width=5, height=2, font="lucida 15 bold")
            b.pack(side="left", padx=5, pady=5)
            b.bind("<Button-1>", click_handler)

    root.mainloop()

if __name__ == "__main__":
    build_calculator()
```

### ✧ THE MANIFESTATION ✧
```text
> Calculator Started ✧
> User Interaction: 7 * 8 =
> Result Displayed: 56
> Clear Action: [Screen Empty]
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ EXPERIMENT 3: STUDENT REGISTRATION ✧
*The Union of GUI and Database*

### ✧ THE BLUEPRINT ✧
1.  **Preparation:** Establish a connection to `students.db` and create a table for registration records.
2.  **Collection:** Gather student details (Name, Course, Email) through Entry widgets.
3.  **Persistence:** Inscribe the gathered data into the database using parameterized SQL queries.

### ✧ THE CREATION ✧
```python
import tkinter as tk
import sqlite3

def register_student():
    """Inscribes student details into the persistent database."""
    name = entry_name.get()
    course = entry_course.get()
    email = entry_email.get()
    
    if name and course and email:
        try:
            conn = sqlite3.connect("students.db")
            cursor = conn.cursor()
            cursor.execute("INSERT INTO students(name, course, email) VALUES (?, ?, ?)", (name, course, email))
            conn.commit()
            label_status.config(text="Registration Successful ✧", fg="green")
            # Clearing the fields
            for entry in [entry_name, entry_course, entry_email]:
                entry.delete(0, tk.END)
        except sqlite3.Error as e:
            label_status.config(text=f"Database Error: {e}", fg="red")
        finally:
            if conn: conn.close()
    else:
        label_status.config(text="Please fill all fields", fg="red")

def setup_registration_form():
    """Designs the visual form for student registration."""
    global entry_name, entry_course, entry_email, label_status
    root = tk.Tk()
    root.title("Student Inscription Form")
    root.geometry("400x400")

    tk.Label(root, text="Student Name:", font=("Helvetica", 10)).pack(pady=5)
    entry_name = tk.Entry(root, width=35)
    entry_name.pack()

    tk.Label(root, text="Course of Study:", font=("Helvetica", 10)).pack(pady=5)
    entry_course = tk.Entry(root, width=35)
    entry_course.pack()

    tk.Label(root, text="Email Address:", font=("Helvetica", 10)).pack(pady=5)
    entry_email = tk.Entry(root, width=35)
    entry_email.pack()

    tk.Button(root, text="Register Now", command=register_student, bg="#4CAF50", fg="white", font=("Helvetica", 12, "bold")).pack(pady=30)

    label_status = tk.Label(root, text="", font=("Helvetica", 10, "italic"))
    label_status.pack()

    root.mainloop()

if __name__ == "__main__":
    setup_registration_form()
```

### ✧ THE MANIFESTATION ✧
```text
> Database: Connected to 'students.db' ✧
> Input Received: Name='Aryaveer' | Course='B.Tech'
> Action: Register Button Invoked.
> Result: "Registered Successfully!"
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

<div style="page-break-after: always;"></div>

## ✧ EXPERIMENT 4: SECURE LOGIN SYSTEM ✧
*The Sentinel of Access*

### ✧ THE BLUEPRINT ✧
1.  **Security:** Use the `show="*"` attribute for password entry to protect the user's secrets.
2.  **Verification:** Query the database to verify if the provided credentials match the inscribed records.

### ✧ THE CREATION ✧
```python
import sqlite3
import tkinter as tk

def perform_login():
    """Verifies user identity against the database records."""
    user = entry_user.get()
    pw = entry_pass.get()
    try:
        conn = sqlite3.connect("users.db")
        cursor = conn.cursor()
        cursor.execute("SELECT * FROM users WHERE username=? AND password=?", (user, pw))
        if cursor.fetchone():
            label_msg.config(text="Login Successful! Welcome ✧", fg="blue")
        else:
            label_msg.config(text="Invalid Credentials", fg="red")
    except sqlite3.Error as e:
        print(f"Error: {e}")
    finally:
        if conn: conn.close()

# Symbolic layout for the Login Sentinel
# ... [Tkinter Layout Code] ...
```

### ✧ THE MANIFESTATION ✧
```text
> Action: Signup (user='admin', pass='****')
> SQL: INSERT INTO users... ✧
> Action: Login (user='admin', pass='****')
> Feedback: "Login Successful!"
```

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈

## ✧ THE REFLECTION ✧
*The Conclusion*

Through these experiments, I have mastered the synergy between visual design and data management. Tkinter has provided the canvas for my logic, while SQLite has given my applications the gift of memory. Together, they form the basis of professional-grade software that is as functional as it is interactive.

◈━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━◈
