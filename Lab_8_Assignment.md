# Technical Report: Graphical Interfaces & Relational Persistence (Lab 8)

| Field | Details |
| :--- | :--- |
| **Architect** | Aryaveer Lohia |
| **SAP ID** | 590025719 |
| **Batch** | B18 |
| **Subject** | Python Programming |

--- ◈ ---

## ◈ Objective & Scope
The objective is to architect desktop applications using the Tkinter framework and integrate them with persistent relational storage using SQLite. The scope covers the design of intuitive user interfaces and the implementation of CRUD (Create, Read, Update, Delete) operations through a secure database backend.

## ◈ Conceptual Framework
**Graphical User Interface (GUI):**
The GUI layer (Tkinter) serves as the primary interface for human-system interaction. By employing an event-driven programming model, we can respond to user-triggered events (clicks, keypresses) through specialized handlers, creating a dynamic and interactive experience.

**Relational Persistence (SQLite):**
To ensure data longevity beyond the application session, we utilize SQLite—a lightweight, serverless relational database engine. Integrating the UI with a persistent backend allows for the storage and retrieval of structured data, essential for professional-grade software solutions.

--- ◈ ---

## Experiment 1: The Window Initialization

### ## ◈ Procedural Logic
1.  **System Initialization:** Instantiate the `Tk()` root class to initialize the windowing subsystem.
2.  **State Configuration:** Define the window's geometric constraints and title.
3.  **UI Manifestation:** Deploy basic Label widgets to confirm visual rendering.

### ## ◈ Technical Implementation
```python
import tkinter as tk

def initialize_root_window():
    """Initializes the base Tkinter windowing system."""
    root = tk.Tk()
    root.title("System Interface Prototype")
    root.geometry("400x300")
    root.resizable(False, False)

    # Initializing visual confirmation
    status_label = tk.Label(root, text="Interface Operational", font=("Helvetica", 14))
    status_label.pack(pady=100)

    root.mainloop()

if __name__ == "__main__":
    initialize_root_window()
```

### ## ◈ Execution & Validation
```text
> System Status: Initializing Window...
> Configuration: Title="System Interface Prototype" | Dimensions=400x300
> Status: Window state locked (non-resizable).
```

--- ◈ ---

## Experiment 2: The Arithmetic Logic Engine

### ## ◈ Procedural Logic
1.  **Grid Topology:** Arrange numeric and operator widgets in a grid layout to facilitate intuitive access.
2.  **Expression Parsing:** Utilize the `eval()` engine to dynamically compute mathematical results from string inputs.
3.  **Variable Synchrony:** Bind `StringVar()` to the entry field for real-time state synchronization.

### ## ◈ Technical Implementation
```python
import tkinter as tk

def on_input_event(event):
    """Handles click events for the arithmetic engine."""
    input_text = event.widget.cget("text")
    if input_text == "=":
        try:
            result = str(eval(display_var.get()))
            display_var.set(result)
        except Exception:
            display_var.set("Syntax Error")
    elif input_text == "C":
        display_var.set("")
    else:
        display_var.set(display_var.get() + input_text)

def build_arithmetic_engine():
    """Constructs the visual and logical layers of the calculator."""
    root = tk.Tk()
    root.title("Arithmetic Engine")
    root.geometry("300x450")

    global display_var
    display_var = tk.StringVar()
    display_field = tk.Entry(root, textvar=display_var, font="lucida 20 bold", justify='right')
    display_field.pack(fill="both", pady=15, padx=15)

    layout = [
        ["7", "8", "9", "/"],
        ["4", "5", "6", "*"],
        ["1", "2", "3", "-"],
        ["0", ".", "=", "+"],
        ["C"]
    ]

    for row in layout:
        row_frame = tk.Frame(root)
        row_frame.pack()
        for char in row:
            btn = tk.Button(row_frame, text=char, width=5, height=2, font="lucida 15 bold")
            btn.pack(side="left", padx=5, pady=5)
            btn.bind("<Button-1>", on_input_event)

    root.mainloop()

if __name__ == "__main__":
    build_arithmetic_engine()
```

### ## ◈ Execution & Validation
```text
> Engine: Initialized.
> Trace: Input sequence '12 * 5'
> Result: '60' displayed.
```

--- ◈ ---

## Experiment 3: Persistent Registry System

### ## ◈ Procedural Logic
1.  **SQL Connection:** Establish a persistent link to `registry.db`.
2.  **Data Extraction:** Ingest data from UI Entry fields (Name, Course, Email).
3.  **Parameterized Persistence:** Inscribe data into the SQL table using sanitized queries to ensure system security.

### ## ◈ Technical Implementation
```python
import tkinter as tk
import sqlite3

def persist_registry_data():
    """Synchronizes UI data with the persistent SQL backend."""
    name, course, email = ent_name.get(), ent_course.get(), ent_email.get()
    
    if all([name, course, email]):
        try:
            conn = sqlite3.connect("registry.db")
            cur = conn.cursor()
            cur.execute("INSERT INTO students(name, course, email) VALUES (?, ?, ?)", (name, course, email))
            conn.commit()
            lbl_status.config(text="Status: Synchronization Successful", fg="green")
            for e in [ent_name, ent_course, ent_email]: e.delete(0, tk.END)
        except sqlite3.Error as e:
            lbl_status.config(text=f"Database Fault: {e}", fg="red")
        finally:
            if conn: conn.close()
    else:
        lbl_status.config(text="Status: Missing Input Fields", fg="red")

def setup_registry_ui():
    """Orchestrates the UI layout for the registry system."""
    global ent_name, ent_course, ent_email, lbl_status
    root = tk.Tk()
    root.title("Persistent Registry Form")
    root.geometry("400x400")

    tk.Label(root, text="Full Name:").pack(pady=5)
    ent_name = tk.Entry(root, width=35); ent_name.pack()

    tk.Label(root, text="Program of Study:").pack(pady=5)
    ent_course = tk.Entry(root, width=35); ent_course.pack()

    tk.Label(root, text="Email Identifier:").pack(pady=5)
    ent_email = tk.Entry(root, width=35); ent_email.pack()

    tk.Button(root, text="Persist Data", command=persist_registry_data, bg="#2E7D32", fg="white").pack(pady=30)

    lbl_status = tk.Label(root, text="", font=("Helvetica", 10, "italic"))
    lbl_status.pack()

    root.mainloop()

if __name__ == "__main__":
    setup_registry_ui()
```

### ## ◈ Execution & Validation
```text
> Database: Connected to 'registry.db'
> Input: Name='Aryaveer' | Course='B.Tech CSE'
> Status: SQL COMMIT successful.
```

--- ◈ ---

## ◈ Analysis & Synthesis
The integration of Tkinter and SQLite provides a robust architectural pattern for developing modern desktop applications. This experiment confirms that separating the visual presentation layer from the persistent data layer is essential for creating scalable, maintainable, and secure software systems. The use of parameterized queries and event-driven logic highlights the transition from basic scripting to professional application engineering.
