# 👟 Threat Model Analysis: Sneaker Trading Mobile App (PASTA Framework)

## 📌 Executive Summary
I performed a comprehensive threat model for a new mobile application designed for sneaker collectors to buy and sell shoes. Using the **PASTA (Process for Attack Simulation and Threat Analysis)** framework, I evaluated the application’s security requirements across all seven stages to ensure a secure launch and protect user data privacy.

---

## 🏗️ Stage I: Define Business Objectives
To align security with business goals, I identified the following key objectives:
* **Data Privacy:** Ensuring users feel confident that their personal and financial information is handled responsibly.
* **Transaction Integrity:** Facilitating clear, quick, and secure payment processing to avoid legal and financial liabilities.
* **User Trust:** Implementing a seller rating system and secure direct messaging to encourage a safe community environment.

---

## 🛠️ Stage II: Technical Scope & Prioritization
The application utilizes several core technologies. I prioritized the evaluation of **SQL (Structured Query Language)** and **APIs**:
* **Rationale:** SQL is the backbone of the sneaker inventory and user database. If misconfigured, it is vulnerable to **SQL Injection**, which could lead to a total data breach. APIs are equally critical as they manage the interaction between the app and third-party payment processors; any vulnerability here could expose credit card data in transit.

* ---

## 📊 Stage III & VI: Decomposition & Attack Modeling
I analyzed the data flow to understand how the application handles information during a product search.



By building an **Attack Tree**, I mapped out how a threat actor might attempt to reach sensitive user data:
* **Primary Goal:** Access User Data.
* **Vectors:** SQL Injection (exploiting a lack of prepared statements), Session Hijacking, or exploiting weak login credentials.



---

## 🛡️ Stage IV, V & VII: Threats, Vulnerabilities, & Defenses
I identified specific risks and mapped them to defensive controls.

### 1. Threats & Vulnerabilities
* **External Threat:** A malicious actor using a virus to attack the authentication system.
* **Internal/Social Threat:** A threat actor using social engineering against an employee to gain backend access.
* **Vulnerability:** Unencrypted payment forms that could allow for the sniffing of credit card numbers.
* **Vulnerability:** Lack of input validation in search bars, making the database susceptible to SQLi.

### 2. Recommended Security Controls (Remediation)
To mitigate these risks, I recommend the following defenses:
* **Input Validation & Prepared Statements:** To neutralize the risk of SQL injection attacks.
* **Encryption (AES & RSA):** Utilizing PKI to secure data at rest and in transit.
* **Multi-Factor Authentication (MFA):** To protect user accounts even if passwords are compromised.
* **Secure API Integration:** Ensuring all third-party components use tokenization for payment handling.

---
**Source:** This threat modeling lab is based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
