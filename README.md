# cyber-awareness-chatbot
POE
# 🛡️ Cybersecurity Awareness Chatbot

## 📌 Part 3 / POE – All Learning Units

A WPF desktop chatbot application built in **C# (.NET)** with **MySQL database integration**, designed to educate users about cybersecurity threats, safe online behaviour, and security best practices.

---

## 📋 Project Overview

The Cybersecurity Awareness Chatbot helps users improve their online safety by providing:

* 💬 Intelligent chatbot responses using keyword-based NLP simulation
* 🗂️ Task management system with full MySQL CRUD functionality
* 🧠 Cybersecurity quiz game with scoring and feedback
* 😊 Sentiment detection (happy, confused, angry, worried, etc.)
* 📜 Activity logging system for user actions

---

## 🚀 Features

### 🧩 Task 1 – Enhanced GUI (WPF Interface)

* Modern dark-themed WPF UI
* Sidebar navigation (Chat, Tasks, Quiz, Activity Log)
* ASCII header branding
* Welcome sound on startup
* Styled chat bubbles with user/bot colors
* Responsive layout design

---

### 🗄️ Task 2 – MySQL Database Integration (CRUD)

The system manages cybersecurity tasks stored in MySQL.

#### ✔ Features:

* Create tasks
* Read/display tasks
* Update task completion status
* Delete tasks

#### 📌 Database Table:

```sql
CREATE TABLE IF NOT EXISTS tasks (
    Id INT AUTO_INCREMENT PRIMARY KEY,
    Title VARCHAR(255) NOT NULL,
    Description TEXT,
    ReminderDate DATETIME NULL,
    IsCompleted BOOLEAN DEFAULT FALSE,
    CreatedDate DATETIME DEFAULT CURRENT_TIMESTAMP
);
```

#### 📌 Connection String:

```csharp
Server=localhost;Database=cybersecurity_chatbot;Uid=root;Pwd=YOUR_PASSWORD;
```

---

### 🧠 Task 3 – NLP Simulation Engine

The chatbot simulates Natural Language Processing using:

* Keyword-based intent detection
* Task extraction from sentences
* Date interpretation:

  * “tomorrow”
  * “next week”
  * “in 3 days”
* Sentiment analysis:

  * happy 😊
  * angry 😡
  * worried 😟
  * confused 😕
* Memory for user preferences and follow-ups
* Stop-word filtering

---

### 🎮 Task 4 – Cybersecurity Quiz Game

* 14 total questions
* Random selection of 10 questions per quiz
* Multiple choice + True/False questions
* Score tracking system
* Explanations for each answer
* Performance rating:

  * Excellent
  * Good
  * Keep Learning
  * At Risk

---

## 🛠️ Technologies Used

| Technology         | Purpose                   |
| ------------------ | ------------------------- |
| C#                 | Core programming language |
| WPF (XAML)         | User interface            |
| .NET Framework     | Application runtime       |
| MySQL              | Database system           |
| MySql.Data (NuGet) | Database connector        |
| Git & GitHub       | Version control           |

---

## 📁 Project Structure

```
list_view_chats
│
├── Models
│   ├── CyberTask.cs
│   ├── QuizQuestion.cs
│   ├── QuizResult.cs
│   ├── ActivityLogEntry.cs
│
├── Managers
│   ├── TaskManager.cs
│   ├── QuizManager.cs
│   ├── ActivityLogger.cs
│
├── MainWindow.xaml
├── MainWindow.xaml.cs
├── App.xaml
└── App.xaml.cs
```

---

## ⚙️ Setup Instructions

### 📌 Requirements

* Visual Studio 2022
* .NET Framework 4.7.2+
* MySQL Server (XAMPP or Workbench)
* NuGet Package: MySql.Data

---

### 📥 Installation Steps

1. Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/Cybersecurity-Awareness-Chatbot.git
```

2. Open:

```
list_view_chats.sln
```

3. Install MySQL connector:

```bash
Install-Package MySql.Data
```

4. Create database:

```sql
CREATE DATABASE cybersecurity_chatbot;
```

5. Run your application in Visual Studio

---

## 💬 Chat Commands Supported

* add task [name]
* show tasks
* complete task [id]
* delete task [id]
* remind me to [task]
* start quiz
* show log
* help

---

## 🛡️ Security Focus Areas

* Password safety
* Phishing awareness
* Social engineering detection
* VPN usage
* Two-factor authentication
* Safe browsing habits

---

## 👨‍💻 Author

Cybersecurity Awareness Chatbot – POE Project
Built using WPF + C# + MySQL
