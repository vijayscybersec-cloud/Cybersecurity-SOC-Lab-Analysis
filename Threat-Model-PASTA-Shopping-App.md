# 👟 Threat Model Analysis: Sneaker Trading Mobile App (PASTA Framework)

## 📌 Executive Summary
I performed a comprehensive threat model for a new mobile application designed for sneaker collectors. Using the **PASTA (Process for Attack Simulation and Threat Analysis)** framework, I evaluated the application’s security requirements across all seven stages to ensure a secure launch and protect user data privacy.

---

## 🏗️ Stage I: Define Business & Security Objectives
To align security with business goals, I identified the following key requirements:
* **Account Management:** Users must be able to create member profiles internally or by connecting external accounts.
* **Financial Transactions:** The app must securely process payments between buyers and sellers.
* **Compliance:** The application must maintain compliance with **PCI-DSS** standards for handling financial data.

---

## 🛠️ Stage II: Technical Scope
The application utilizes a modern tech stack (API, PKI, AES, SHA-256, SQL). I prioritized the evaluation of **APIs**:
* **Rationale:** APIs facilitate the exchange of data between customers, partners, and employees. They handle high volumes of PII and financial information, creating a large attack surface that must be prioritized for security testing.

---

## 📊 Stage III & VI: Decomposition & Attack Modeling
I analyzed the data flow to understand how the application handles information during a product search.



By building an **Attack Tree**, I mapped out how a threat actor might attempt to reach sensitive user data:
* **Primary Goal:** Compromise User Data.
* **Attack Vectors:** SQL Injection (exploiting a lack of prepared statements) and Session Hijacking (via broken API tokens).



---

## 🛡️ Stage IV, V & VII: Risk Analysis & Countermeasures
I identified specific risks and mapped them to defensive controls.

### 1. Threats & Vulnerabilities
* **Key Threats:** Injection attacks and Session hijacking.
* **Vulnerabilities:** A lack of prepared statements in the codebase and broken API tokens.

### 2. Recommended Security Controls (Defense-in-Depth)
To mitigate these risks, I recommend implementing the following safeguards:
* **SHA-256 Hashing:** To protect sensitive user credentials and passwords.
* **Principle of Least Privilege (PoLP):** Ensuring the application only has the minimum necessary access to database resources.
* **Incident Response Procedures:** Establishing clear steps to take if a breach is detected.
* **Password Policy:** Enforcing complexity and rotation requirements for all user accounts.

---
**Source:** This threat modeling lab is based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
