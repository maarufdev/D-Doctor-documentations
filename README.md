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
---

## 🩺 Project Overview

The **E-Doctor App** consists of two major modules:

### 👨‍⚕️ Admin Module
- Admin Manage Users
  <img width="1904" height="990" alt="image" src="https://github.com/user-attachments/assets/5eb67aeb-3118-4f95-be23-fd2c67c9e62c" />
  <img width="1908" height="999" alt="image" src="https://github.com/user-attachments/assets/55bae9a9-58bf-4fad-96a2-a99a0dd67699" />
  <img width="1901" height="1018" alt="image" src="https://github.com/user-attachments/assets/d57e222e-36b6-498e-ad51-ead0324fb063" />
  <img width="1902" height="957" alt="image" src="https://github.com/user-attachments/assets/eb4eb02d-bff5-4622-8939-9a817a016ab0" />

- User Activites
  <img width="1906" height="961" alt="image" src="https://github.com/user-attachments/assets/cf88c82f-8a6f-47e2-baf2-531a33590fb0" />

### 🧍‍♂️ Patient Module
- Patient User Activites
  <img width="1895" height="968" alt="image" src="https://github.com/user-attachments/assets/8c28c0d6-daf0-48c4-a342-d0ebbc14b982" />
---

## 🏗️ Architecture

The **E-Doctor App** follows **Clean Architecture**, ensuring a maintainable, testable, and modular structure.

### 🧱 Layered Structure

