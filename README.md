# 💳 ATM Web Application (Python Full Stack)

This project is a **web-based ATM system** developed using **Python Flask**, **MySQL**, and **HTML/CSS**. The system allows users to deposit money, withdraw funds, generate PINs, and view mini-statements for their accounts.

---

## 🚀 Features

* 🔐 **PIN Generation** for new accounts
* 💸 **Deposit** funds into an account
* 💳 **Withdraw** money with PIN validation
* 📋 **Mini Statement** displaying account details
* ⚙️ Backend powered by **Flask** and **MySQL**
* 🎨 Simple inline CSS styling without JavaScript

---

## 🛠️ Technologies Used

* **Python 3.x**
* **Flask**
* **PyMySQL**
* **MySQL**
* **HTML** (with inline CSS)

---

## 🗂️ Project Structure

```
atm_app/
├── templates/
│   ├── home.html
│   ├── deposit1.html
│   ├── withdraw1.html
│   ├── withdraw2.html
│   ├── ministatement1.html
│   ├── ministatement2.html
│   ├── pingeneration1.html
│   ├── pingeneration2.html
├── app.py
└── README.md
```

---

## 🧱 Database Schema

Database: `ATM`
Table: `ACCOUNTS`

```sql
CREATE TABLE ACCOUNTS (
    USER_ACCNO VARCHAR(20) PRIMARY KEY,
    USER_NAME VARCHAR(50),
    USER_EMAIL VARCHAR(100),
    USER_PHONE VARCHAR(15),
    USER_ADDRESS TEXT,
    USER_PIN INT,
    USER_BALANCE INT
);
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/atm-web-app.git
cd atm-web-app
```

### 2. Setup the MySQL Database

* Open MySQL and run the table creation script above.
* Insert some test records into the `ACCOUNTS` table if needed.

### 3. Configure DB credentials

In `app.py`, edit the `db_config` dictionary with your MySQL settings:

```python
db_config = {
    "host" : "localhost",
    "user" : "root",
    "password" : "Root",
    "database" : "ATM"
}
```

### 4. Install Python dependencies

```bash
pip install flask pymysql
```

### 5. Run the Flask App

```bash
python app.py
```

Access the application at [http://localhost:5000](http://localhost:5000)

---

## 📷 Screenshots

> You can add screenshots of your HTML pages here.

---

## 💡 Notes

* No JavaScript is used — the UI is simple and handled via HTML forms and inline CSS.
* This is a learning project and should be expanded for production use with security, validations, and error handling.
