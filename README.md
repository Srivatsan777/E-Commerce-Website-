<h1 align=center>E-Commerce Website</h1>

Simple e-commerce website built with Flask and SQLite. Allows users to register, login, and purchase items. Also has an admin panel that allows administrators to view and manage users and items.

<h2 align=center>Go to the website<br>https://e-commerce2023.onrender.com</h2>

### Dependencies
- Flask >= 2.2.5
- SQLAlchemy >= 2.0.21
- Flask-WTF >= 1.1.1
- WTForms >= 3.0.1
- Flask-Bcrypt >= 1.0.1
- Flask-Login >= 0.6.2
- gunicorn >= 21.2.0

---

### Installation
#### 1. Install the dependencies.
> ```
> pip install -r requirements.txt
> ```

#### 2. Create a database.
> ```
> sqlite3 e-commerce.db
> ```

#### 3. Create the tables.
> ```
> CREATE TABLE users (
>     id INTEGER PRIMARY KEY AUTOINCREMENT,
>     username TEXT UNIQUE NOT NULL,
>     email_address TEXT UNIQUE NOT NULL,
>     password_hash TEXT NOT NULL,
>     budget INTEGER NOT NULL DEFAULT 10000
> );
>
> CREATE TABLE items (
>     id INTEGER PRIMARY KEY AUTOINCREMENT,
>     name TEXT UNIQUE NOT NULL,
>     barcode TEXT UNIQUE NOT NULL,
>     price INTEGER NOT NULL,
>     description TEXT NOT NULL,
>     owner INTEGER REFERENCES users (id)
> );
> ```

#### 4. Run the website.
> ```
> python main.py
> ```

---

### Usage
> Register for an account.

> Login to your account.

> Browse the items for sale.

> Add items to your cart.

> Checkout and pay for your items.

---

### Admin Panel
The admin panel allows administrators to view and manage users and items. It also has two tabs: "Control Users" and "Control Items" to easily view and manage.
  * Username: admin
  * Password: admin

---
