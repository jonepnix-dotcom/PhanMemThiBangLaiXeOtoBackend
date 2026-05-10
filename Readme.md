# 🚗 PhanMemThiBangLaiXeOtoBackend

Backend system for an online automobile driving license exam application.
This project provides REST APIs, authentication, exam management, and database backup/restore support using SQL Server.

---

# 📌 Project Overview

This backend system supports a driving license learning platform including:

* User authentication & authorization
* Driving theory exam management
* Question bank management
* Exam scoring system
* Real-time exam data handling (API-based)
* SQL Server database backup/restore integration

---

# 🚀 Technologies Used

## Backend

* ASP.NET Core Web API
* Entity Framework Core
* LINQ
* Dependency Injection

## Database

* Microsoft SQL Server
* Database Backup (.bak file support)

## Tools

* Visual Studio 2022
* SQL Server Management Studio (SSMS)
* Git & GitHub
* Postman

---

# 🗄️ Database Setup (IMPORTANT)

This project uses a **pre-built SQL Server backup file (.bak)**.

## 📂 Step 1: Locate backup file

Database backup is included in:

```bash id="db1"
/Database/BackenDatabase.bak
```

or downloaded from repository.

---

## 📥 Step 2: Restore database in SQL Server

Open **SQL Server Management Studio (SSMS)** and run:

```sql id="db2"
RESTORE DATABASE BackenDatabase
FROM DISK = 'YOUR_PATH\BackenDatabase.bak'
WITH REPLACE;
```

Example:

```sql id="db3"
RESTORE DATABASE BackenDatabase
FROM DISK = 'D:\Backup\BackenDatabase.bak'
WITH REPLACE;
```

---

## ⚠️ Step 3: Check logical file (if error occurs)

```sql id="db4"
RESTORE FILELISTONLY
FROM DISK = 'D:\Backup\BackenDatabase.bak';
```

---

# ⚙️ Configuration

## Update connection string in `appsettings.json`

```json id="cfg1"
"ConnectionStrings": {
  "MyConnect": "Data Source=localhost;Initial Catalog=dbthi_banglai;User ID=sa;Password=YOUR_PASSWORD;TrustServerCertificate=True"
}
```

---

# 🚀 Run Project

## 1. Build project

```bash id="run1"
dotnet build
```

---

## 2. Run project

```bash id="run2"
dotnet run
```

or press:

```text id="run3"
F5 (Visual Studio)
```

---

# 📡 API Features

* User login/register
* Get exam questions
* Submit exam answers
* Calculate score
* Manage question bank (Admin)
* Manage exams (Admin)

---

# 🧠 Learning Outcomes

This project helped improve:

* ASP.NET Core Web API development
* SQL Server backup/restore workflow
* RESTful API design
* Database design for exam systems
* Authentication & authorization concepts
* Clean backend architecture

---

# 🔗 Repository

* GitHub: https://github.com/jonepnix-dotcom/PhanMemThiBangLaiXeOtoBackend

---

# 👨‍💻 Author

* GitHub: https://github.com/jonepnix-dotcom
* Email: [jonepnix@gmail.com](mailto:jonepnix@gmail.com)

---

# 📄 License

This project is for learning and portfolio purposes only.
