---

# 🔐 Secure User Authentication System

This project implements a **Secure User Authentication System** as part of a Full Stack Web Development task. The system allows users to **register, log in securely, and access protected routes** using token-based authentication, while storing user data in an **SQL database (MySQL)**.

---

## 📌 Features

* User registration with secure password hashing
* Secure login with credential validation
* JWT-based authentication and session management
* Protected routes accessible only to authenticated users
* SQL database integration using MySQL

---

## 🛠️ Apps / Tools Used

* **VS Code** – Code editor
* **Node.js (LTS)** – Backend runtime
* **MySQL** – SQL database
* **MySQL Workbench** – Database management
* **Postman** – API testing
* **Browser (Chrome / Edge)** – Frontend testing

---

## 🧱 Tech Stack

* **Frontend**: HTML, CSS, JavaScript
* **Backend**: Node.js, Express
* **Database**: MySQL (SQL)
* **Authentication**: bcrypt, JWT
* **Security**: Password hashing and protected routes

---

## 📁 Project Structure

```
secure-auth-sql/
│
├── server.js
├── db.js
├── package.json
├── .env
│
├── routes/
│   └── auth.js
│
├── middleware/
│   └── authMiddleware.js
│
└── frontend/
    ├── register.html
    ├── login.html
    └── dashboard.html
```

---

## 🗄️ Database Setup (MySQL)

Create the database and table using MySQL Workbench:

```sql
CREATE DATABASE auth_system;
USE auth_system;

CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100) UNIQUE,
  password VARCHAR(255),
  role VARCHAR(20) DEFAULT 'user'
);
```

---

## ⚙️ Backend Setup

### 1️⃣ Install Dependencies

```bash
npm install
```

### 2️⃣ Configure Environment Variables

Create a `.env` file:

```env
JWT_SECRET=securekey123
```

### 3️⃣ Update Database Credentials

Edit `db.js` and add your MySQL password.

### 4️⃣ Start the Server

```bash
node server.js
```

Server runs on:

```
http://localhost:5000
```

---

## 🌐 Frontend Usage

1. Open `frontend/register.html` in a browser
2. Register a new user
3. Open `frontend/login.html` and log in
4. Open `frontend/dashboard.html` to access the protected route

Only authenticated users can view the dashboard.

---

## ✅ Task Requirements Fulfilled

* ✔ Secure login and registration
* ✔ SQL database usage (MySQL)
* ✔ Password hashing with bcrypt
* ✔ JWT-based session management
* ✔ Protected routes
* ✔ Matches the given task description

---

## 🧠 Submission Summary

Implemented a secure user authentication system using Node.js, Express, and MySQL with password hashing, JWT-based session management, and protected routes to ensure authorized access.

---
