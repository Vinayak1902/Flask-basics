# Flask Framework – Key Features

Flask has two very important components:

---

## 1️⃣ WSGI – Web Server Gateway Interface

WSGI stands for **Web Server Gateway Interface**.

It acts as a **bridge** between:

- Your Python application (Flask, Django, etc.)
- A web server (nginx, Apache, Gunicorn)

### ⭐ Simple Explanation

- Python speaks **Python language**
- Web servers speak **HTTP language**
- They cannot communicate directly

🔥 **WSGI works as the translator** between them.

WSGI decides how:

- The server should send requests to Python
- Python should send responses back to the server

### ⭐ Why We Need WSGI?

Python alone **cannot handle web traffic**.  
If your application receives many requests:

- Server → WSGI → Python App → WSGI → Server → User

WSGI ensures smooth two-way communication.

---

## 2️⃣ Jinja2 Template Engine

Jinja2 is a **template engine** used with Flask to create **dynamic HTML pages**.

Think of it like this:

🔥 **Jinja2 = HTML + Python together**

It allows you to write HTML and insert:

- Variables  
- Loops  
- Conditions  
- Data from Python code  

### ⭐ Why We Need Jinja2?

HTML by itself is **static**:

```html
<p>Hello Vinayak</p>
But Jinja2 makes HTML dynamic, allowing it to change based on Python data.

Examples of usage:

Show username

Display list values

Show database records

Generate tables

💡 Example — Variable Rendering With Jinja2
HTML Template (index.html)
<p>Hello {{ name }}!</p>

Flask Code
from flask import Flask, render_template

app = Flask(__name__)

@app.route('/')
def home():
    return render_template("index.html", name="Vinayak")

Output
Hello Vinayak!


Here, {{ name }} is replaced with "Vinayak" by Jinja2.


If you want, I can also make:  
✔ a shorter summarised README  
✔ a decorated README with emojis  
✔ or add a Table of Contents  

Just tell me!