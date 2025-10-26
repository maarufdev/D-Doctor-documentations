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

- **[Microsoft SQL Server 2019+](https://go.microsoft.com/fwlink/p/?linkid=2216019&clcid=0x409&culture=en-us&country=us)**
- **[Microsoft SQL Server Management Studio (SSMS)](https://aka.ms/ssmsfullsetup)**
- **.NET 8 SDK or later**
- **Visual Studio 2022 (with ASP.NET and web development workload)**
---
# 🧱 Microsoft SQL Server Installation & Configuration Guide

Follow this step-by-step guide to install and configure **Microsoft SQL Server** and **SQL Server Management Studio (SSMS)** for your development environment.

---

## 🔽 Step 1: Download Required Tools

- **Microsoft SQL Server 2019 (or later)**  
  👉 [Download SQL Server](https://go.microsoft.com/fwlink/p/?linkid=2216019&clcid=0x409&culture=en-us&country=us)

- **SQL Server Management Studio (SSMS)**  
  👉 [Download SSMS](https://aka.ms/ssmsfullsetup)

---

## ⚙️ Step 2: Install Microsoft SQL Server

1. Run the installer file (`SQLServer2019-SSEI-Dev.exe` or later).
2. Choose **Basic** installation.
3. On the **Feature Selection** screen, ensure **Database Engine Services** is checked.
4. Continue to **Instance Configuration** — you can keep **Default instance (MSSQLSERVER)**.
5. In **Server Configuration**, click **Next**.
6. In **Database Engine Configuration**:
   - Select **Mixed Mode (SQL Server authentication and Windows authentication)**.
   - Enter a password for the `sa` (System Administrator) account:  
     ```
     Username: sa
     Password: P@ssw0rd123!
     ```
   - Click **Add Current User** under *Specify SQL Server administrators*.
7. Proceed to complete the installation.

---

## 🔐 Step 3: Enable SQL Authentication (if not enabled)

If you did not select **Mixed Mode Authentication** during installation:

1. Open **SQL Server Management Studio (SSMS)**.
2. Connect using **Windows Authentication**.
3. Right-click the server name in **Object Explorer** → click **Properties**.
4. Go to **Security** → choose **SQL Server and Windows Authentication mode**.
5. Click **OK**.
6. Restart the SQL Server service:
   - In SSMS: Right-click the server → **Restart**, or  
   - In Windows Services: restart **SQL Server (MSSQLSERVER)**.

---

## 👤 Step 4: Enable and Set Password for `sa` Account

1. In **SSMS**, expand **Security → Logins**.
2. Right-click **sa** → choose **Properties**.
3. Under **General**, set a strong password (e.g. `P@ssw0rd123!`).
4. Under **Status**, ensure:
   - **Login:** Enabled  
   - **Grant:** Connect SQL → Yes  
5. Click **OK** to save changes.

---

## 🧩 Step 5: Test Connection

1. Open **SQL Server Management Studio (SSMS)**.
2. In the connection dialog:
   - **Server type:** Database Engine  
   - **Server name:** `(local)` or `localhost`  
   - **Authentication:** SQL Server Authentication  
   - **Login:** `sa`  
   - **Password:** (your chosen password)
3. Click **Connect**.

✅ If the connection is successful, SQL authentication is configured correctly.

---

## 🧠 Additional Notes

- Always use a **strong password** for the `sa` account.
- For production setups:
  - Disable `sa` login and create a separate SQL user with limited privileges.
  - Use **Windows Authentication** whenever possible for better security.

---

## 🧩 Related Documentation

- [Install .NET 8 SDK](https://dotnet.microsoft.com/en-us/download)
- [Install Visual Studio 2022](https://visualstudio.microsoft.com/downloads/)
- [Install Git](https://git-scm.com/downloads)
- [Official SQL Server Docs](https://learn.microsoft.com/en-us/sql/sql-server/?view=sql-server-ver16)


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

