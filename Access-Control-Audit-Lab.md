# 🕵️ Incident Investigation: Access Control & Insider Threat

## 📌 Executive Summary
I investigated a suspicious payroll incident where an unauthorized deposit was attempted to an unknown bank account ("FAUX_BANK"). By cross-referencing system event logs with the employee directory, I identified a former contractor whose account was still active and possessed excessive administrative privileges. This report outlines the vulnerabilities exploited and provides recommendations to harden the organization's access controls.

---

## 🔍 Investigation Details
### 1. Log Analysis
An examination of the **Event Log** revealed a critical unauthorized action:
* **Date/Time:** 10/03/2023 at 8:29:57 AM
* **Action:** "Payroll event added. FAUX_BANK"
* **User:** `Legal\Administrator`
* **IP Address:** `152.207.255.255`
* **Computer Name:** `Up2-NoGud` (Suspicious hostname)

### 2. Identifying the Threat Actor
By cross-referencing the IP address and username with the **Employee Directory**, I identified the following:
* **User:** Robert Taylor Jr.
* **Role:** Former Legal Attorney (Contractor).
* **Employment Status:** His contract ended on **2019-12-27**, yet the incident occurred in **2023**.
* **Authorization Level:** Still listed as **Admin**.

---

## ⚠️ Access Control Issues
The following security gaps allowed this incident to occur:
1.  **Failure to De-provision:** The account of a former contractor remained active for nearly four years after their end date.
2.  **Excessive Privileges:** A legal attorney was granted **Admin** rights, allowing them to modify payroll records—a violation of the **Principle of Least Privilege (PoLP)**.
3.  **Inadequate Authentication:** The attacker was able to gain access using only a username and password (likely a "ghost account" with a weak or default password).

---

## 🛠️ Mitigations & Recommendations
To prevent future breaches, I recommend the following security controls:

* **Implement a De-provisioning Workflow:** Establish a mandatory HR-to-IT protocol to disable all network access immediately upon a user's departure or contract end date.
* **Enforce Least Privilege:** Conduct a full audit of user permissions. Administrative access to payroll systems must be restricted strictly to HR and Finance roles.
* **Mandate Multi-Factor Authentication (MFA):** Require MFA for all administrative actions to prevent unauthorized access, even if account credentials are compromised.
* **Regular Access Reviews:** Perform quarterly audits of all active accounts to identify and delete "ghost accounts" of former employees.

---
**Source:** This investigation lab and data samples are provided by the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
