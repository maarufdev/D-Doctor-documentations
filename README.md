# 🩺 E-Doctor App Documentation

The **E-Doctor App** is a rule-based medical diagnosis system built using **ASP.NET Core MVC**, **Entity Framework Core**, and **Clean Architecture** principles.  
It enables admins to configure diseases and symptoms, define rules, and allows patients to receive automated diagnostic feedback based on their responses.

---

## 📋 Table of Contents

1. [Requirements](#-requirements)
2. [Project Overview](#-project-overview)
3. [Architecture](#-architecture)
4. [Technology Stack](#-technology-stack)
5. [Installation](#-installation)
6. [Database Configuration](#-database-configuration)
7. [Running the Application](#-running-the-application)
8. [Seeding Admin & Patient Accounts](#-seeding-admin--patient-accounts)
9. [Contributing](#-contributing)
10. [License](#-license)
11. [Resources & References](#-resources--references)

---

## ⚙️ Requirements

Before running the project, ensure the following software is installed on your machine:

- **Microsoft SQL Server 2019+**
- **Microsoft SQL Server Management Studio (SSMS)**
- **.NET 8 SDK or later**
- **Visual Studio 2022 (with ASP.NET and web development workload)**
- **Git**

📸 _Example setup screenshots:_

![SQL Server](docs/images/sql-server.png)
![SSMS](docs/images/ssms.png)

---

## 🩺 Project Overview

The **E-Doctor App** consists of two major modules:

### 👨‍⚕️ Admin Module
- Manage diseases and associated symptoms  
- Configure rule-based logic for diagnosis  
- Monitor user activity logs  
- Test configured rules with sample questions  

### 🧍‍♂️ Patient Module
- Perform self-diagnosis through an interactive questionnaire  
- View diagnosis results based on admin-defined rules  
- Manage basic account settings  

---

## 🏗️ Architecture

The **E-Doctor App** follows **Clean Architecture**, ensuring a maintainable, testable, and modular structure.

### 🧱 Layered Structure

