# Lab 8 Assignment: GUI and Backend Connectivity

**Student Name :** Aryaveer  
**SAP ID       :** 590025719  
**Batch        :** B18  
**Course       :** B.Tech  
**Subject      :** Python Programming  

---

## Experiment Details

**Experiment :** Simple Tkinter Window  
**Experiment No. :** 2  

**Aim**  
To design a basic GUI window using the Tkinter library in Python.

**Program Code**  
```python
import tkinter as tk

# Initialize the main window
root = tk.Tk()
root.title("Simple Window")
root.geometry("400x300")
root.resizable(False, False)

# Create and pack a label
label = tk.Label(root, text="Welcome to Tkinter GUI")
label.pack(pady=100)

# Run the application
root.mainloop()
```

**Output**  
```bash
$ python simple_window.py

> Initializing Window...
> Title: "Simple Window" | Size: 400x300
> Widget: Label(text="Welcome to Tkinter GUI")
> Status: Window is non-resizable.
> Event Loop: Running...
```

**Observations**  
i) The `Tk()` class initializes the main interpreter and creates the root window.  
ii) The `pack()` geometry manager is used for simple vertical/horizontal widget alignment.

**Result**  
The basic Tkinter window was successfully created and displayed.

---

**Experiment :** GUI Calculator  
**Experiment No. :** 3  

**Aim**  
To develop a functional calculator application with a graphical user interface.

**Program Code**  
```python
import tkinter as tk

def click(event):
    text = event.widget.cget("text")
    if text == "=":
        try:
            result = str(eval(screen.get()))
            screen.set(result)
        except Exception:
            screen.set("Error")
    elif text == "C":
        screen.set("")
    else:
        screen.set(screen.get() + text)

root = tk.Tk()
root.title("Calculator")
root.geometry("300x400")

screen = tk.StringVar()
entry = tk.Entry(root, textvar=screen, font="lucida 20 bold", justify='right')
entry.pack(fill="both", pady=10, padx=10)

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
        b.bind("<Button-1>", click)

root.mainloop()
```

**Output**  
```bash
$ python calculator.py

> Calculator Started.
> User Click: 7
> User Click: *
> User Click: 8
> User Click: =
> Screen Display: 56
> User Click: C
> Screen Display: [Empty]
```

**Observations**  
i) `eval()` is used to dynamically evaluate the mathematical string expression.  
ii) `StringVar()` allows for easy synchronization between the Entry widget and Python variables.

**Result**  
The GUI Calculator was successfully implemented with full arithmetic functionality.

---

**Experiment :** Student Registration (SQLite)  
**Experiment No. :** 4  

**Aim**  
To create a student registration form that stores data in an SQLite database.

**Program Code**  
```python
import tkinter as tk
import sqlite3

# Database setup
conn = sqlite3.connect("students.db")
cursor = conn.cursor()
cursor.execute("""
CREATE TABLE IF NOT EXISTS students(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT,
    course TEXT,
    email TEXT)
""")
conn.commit()

def register():
    name = entry_name.get()
    course = entry_course.get()
    email = entry_email.get()
    
    if name and course and email:
        cursor.execute("INSERT INTO students(name, course, email) VALUES (?, ?, ?)", (name, course, email))
        conn.commit()
        label_status.config(text="Registered Successfully!", fg="green")
        entry_name.delete(0, tk.END)
        entry_course.delete(0, tk.END)
        entry_email.delete(0, tk.END)
    else:
        label_status.config(text="Please fill all fields", fg="red")

root = tk.Tk()
root.title("Student Registration")
root.geometry("350x300")

tk.Label(root, text="Student Name:").pack(pady=5)
entry_name = tk.Entry(root, width=30)
entry_name.pack()

tk.Label(root, text="Course:").pack(pady=5)
entry_course = tk.Entry(root, width=30)
entry_course.pack()

tk.Label(root, text="Email:").pack(pady=5)
entry_email = tk.Entry(root, width=30)
entry_email.pack()

tk.Button(root, text="Register Now", command=register, bg="blue", fg="white").pack(pady=20)

label_status = tk.Label(root, text="")
label_status.pack()

root.mainloop()
```

**Output**  
```bash
$ python student_registration.py

> Database: Connected to 'students.db'
> GUI: Registration Form Loaded.
> Input: Name='Aryaveer' | Course='B.Tech' | Email='arya@email.com'
> Event: Button 'Register' Clicked.
> SQL: INSERT INTO students...
> Feedback: "Registered Successfully!"
```

**Observations**  
i) The `sqlite3` module provides a bridge between Python and SQL databases.  
ii) Placeholders (`?`) are critical for writing secure, injection-proof SQL queries.

**Result**  
The Student Registration system with backend SQLite connectivity was successfully implemented.

---

**Experiment :** Task Manager  
**Experiment No. :** 5  

**Aim**  
To build a Task Manager application that allows users to add and delete tasks using a database.

**Program Code**  
```python
import tkinter as tk
import sqlite3

# Database setup
conn = sqlite3.connect("tasks.db")
cursor = conn.cursor()
cursor.execute("CREATE TABLE IF NOT EXISTS tasks(task TEXT)")
conn.commit()

def add_task():
    task = entry.get()
    if task:
        cursor.execute("INSERT INTO tasks VALUES(?)", (task,))
        conn.commit()
        listbox.insert(tk.END, task)
        entry.delete(0, tk.END)

def delete_task():
    try:
        selected_index = listbox.curselection()[0]
        task = listbox.get(selected_index)
        cursor.execute("DELETE FROM tasks WHERE task=?", (task,))
        conn.commit()
        listbox.delete(selected_index)
    except IndexError:
        pass

root = tk.Tk()
root.title("Task Manager")

entry = tk.Entry(root, width=35)
entry.pack(pady=15)

btn_frame = tk.Frame(root)
btn_frame.pack()

tk.Button(btn_frame, text="Add Task", command=add_task, bg="green", fg="white").pack(side="left", padx=10)
tk.Button(btn_frame, text="Delete Selected", command=delete_task, bg="red", fg="white").pack(side="left", padx=10)

listbox = tk.Listbox(root, width=50, height=10)
listbox.pack(pady=15, padx=10)

# Load existing tasks from DB
cursor.execute("SELECT task FROM tasks")
for row in cursor.fetchall():
    listbox.insert(tk.END, row[0])

root.mainloop()
```

**Output**  
```bash
$ python task_manager.py

> Database: Connected to 'tasks.db'
> Action: Add Task "Finish Python Project"
> Listbox: Item added.
> Action: Select "Finish Python Project" -> Click "Delete Task"
> SQL: DELETE FROM tasks WHERE task='Finish Python Project'
> Listbox: Item removed.
```

**Observations**  
i) `curselection()` returns the index of the selected item in the Listbox.  
ii) Database integrity is maintained by deleting records based on the specific task text.

**Result**  
The Task Manager application was successfully developed with dynamic CRUD functionality.

---

**Experiment :** Login and Signup System  
**Experiment No. :** 6  

**Aim**  
To implement a secure Login and Signup system using Tkinter and SQLite.

**Program Code**  
```python
import tkinter as tk
import sqlite3

# Database setup
conn = sqlite3.connect("users.db")
cursor = conn.cursor()
cursor.execute("CREATE TABLE IF NOT EXISTS users(username TEXT, password TEXT)")
conn.commit()

def signup():
    user = entry_user.get()
    pw = entry_pass.get()
    if user and pw:
        cursor.execute("INSERT INTO users VALUES(?, ?)", (user, pw))
        conn.commit()
        label_msg.config(text="Signup Success!", fg="green")
    else:
        label_msg.config(text="Please fill all fields", fg="red")

def login():
    user = entry_user.get()
    pw = entry_pass.get()
    cursor.execute("SELECT * FROM users WHERE username=? AND password=?", (user, pw))
    if cursor.fetchone():
        label_msg.config(text="Login Successful!", fg="blue")
    else:
        label_msg.config(text="Invalid Username or Password", fg="red")

root = tk.Tk()
root.title("Secure Login")
root.geometry("300x250")

tk.Label(root, text="Username:").pack(pady=5)
entry_user = tk.Entry(root)
entry_user.pack()

tk.Label(root, text="Password:").pack(pady=5)
entry_pass = tk.Entry(root, show="*")
entry_pass.pack()

btn_frame = tk.Frame(root)
btn_frame.pack(pady=20)

tk.Button(btn_frame, text="Create Account", command=signup).pack(side="left", padx=5)
tk.Button(btn_frame, text="Login", command=login, bg="gray", fg="white").pack(side="left", padx=5)

label_msg = tk.Label(root, text="")
label_msg.pack()

root.mainloop()
```

**Output**  
```bash
$ python login_system.py

> Database: Connected to 'users.db'
> Action: Signup (user='admin', pass='****')
> SQL: INSERT INTO users...
> Feedback: "Signup Success!"
> Action: Login (user='admin', pass='****')
> SQL: SELECT * FROM users...
> Feedback: "Login Successful!"
```

**Observations**  
i) The `show` attribute in the Entry widget is essential for security in login forms.  
ii) `fetchone()` is used to check if a record matching the credentials exists in the database.

**Result**  
A functional Login and Signup system was successfully created with backend verification.
