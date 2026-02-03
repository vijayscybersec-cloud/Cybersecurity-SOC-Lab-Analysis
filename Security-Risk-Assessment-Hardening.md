# 🛡️ Security Risk Assessment & Network Hardening Plan

## 📌 Executive Summary
Following a major data breach at a social media organization that compromised customer PII (names and addresses), I conducted a risk assessment to identify systemic vulnerabilities. This report outlines the critical weaknesses discovered and proposes a multi-layered network hardening strategy to prevent future unauthorized access and data exfiltration.

---

## 🔍 Vulnerability Assessment
During the network inspection, four high-risk vulnerabilities were identified that directly contribute to the organization's insecure security posture:

1. **Password Hygiene:** Employees are currently sharing passwords, which eliminates individual accountability.
2. **Default Credentials:** The administrative password for the database remains set to the factory default.
3. **Weak Perimeter Security:** Firewalls lack defined rules to filter inbound and outbound traffic.
4. **Lack of MFA:** Multi-factor authentication is not implemented, making credential theft easy to exploit.

---

## 🛠️ Proposed Hardening Roadmap
Based on the "Network Hardening Tools" catalog, the following tasks have been prioritized for implementation:

| Hardening Task | Technical Description | Implementation Frequency |
| :--- | :--- | :--- |
| **Multifactor Authentication (MFA)** | Verifying identity in two or more ways (password, OTP, badge, etc.) | Mostly set up once, then maintained. |
| **Port Filtering** | Firewall function that blocks or allows certain port numbers to limit unwanted communication | Executed as needed to control network traffic. |
| **Password Policies** | Focused on salting and hashing passwords (NIST recommendations) | Applied 24/7 to prevent brute force attacks. |
| **Firewall Maintenance** | Checking and updating security configurations regularly | Performed regularly or in response to abnormal traffic. |

---

## 📈 Strategic Hardening Methods

### 1. Strengthening Identity (MFA & Password Policies)
* **Goal:** To prevent attackers from easily guessing user passwords manually or via brute force scripts.
* **Method:** Implement **Multifactor Authentication (MFA)** and **Password Policies** that focus on securing the storage of passwords (salting/hashing) rather than just complexity.
* **Effectiveness:** MFA protects against credential theft by requiring a second factor like a one-time password (OTP) or fingerprint.



### 2. Network Perimeter Defense (Port Filtering & Firewall Maintenance)
* **Goal:** To control network traffic and prevent potential attackers from entering a private network.
* **Method:** Apply **Port Filtering** to block dangerous traffic and perform regular **Firewall Maintenance** to stay ahead of potential threats.
* **Effectiveness:** Disabling unused ports prevents malicious actors from entering the network through open vulnerabilities before an incident occurs.



### 3. Monitoring & Access Control
* **Strategy:** Use **Network Log Analysis** (often via a SIEM) to examine logs and identify events of interest.
* **Strategy:** Define **Network Access Privileges** to limit access to network assets for specific roles or IP addresses, reducing the risk of unauthorized lateral movement.

---

## ✅ Final Conclusion
By implementing these specific hardening tasks—ranging from technical configurations (Port Filtering) to administrative protocols (MFA)—the organization significantly reduces its risk of a secondary data breach. This "Defense in Depth" approach ensures that if one security layer fails, others remain to protect the customer's personal information.

---
**Source:** This risk assessment scenario and the "Network Hardening Tools" reference data are provided by the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
