# 🛡️ Security Risk Assessment & Network Hardening Plan

## 📌 Executive Summary
Following a major data breach at a social media organization that compromised customer PII (names and addresses), I conducted a risk assessment to identify systemic vulnerabilities. This report outlines the critical weaknesses discovered and proposes a multi-layered network hardening strategy to prevent future unauthorized access and data exfiltration.

---

## 🔍 Vulnerability Assessment
During the network inspection, four high-risk vulnerabilities were identified that directly contribute to the organization's insecure security posture:

1. **Password Hygiene:** Employees are currently sharing passwords, eliminating individual accountability.
2. **Default Credentials:** The administrative password for the database remains set to the factory default.
3. **Weak Perimeter Security:** Firewalls lack defined rules to filter inbound and outbound traffic.
4. **Lack of MFA:** Multi-factor authentication is not implemented, making credentials easy to exploit.

---

## 🛠️ Recommended Hardening Tools & Strategies
Based on the organization's needs, I have selected the following hardening tasks from the internal security toolkit:

| Hardening Task | Description | Core Benefit |
| :--- | :--- | :--- |
| **Multifactor Authentication (MFA)** | Requires a user to verify identity in two or more ways (password, OTP, badge, etc.) | Protects against brute force attacks and credential theft. |
| **Port Filtering** | A firewall function that blocks or allows certain port numbers | Limits unwanted communication and prevents attackers from entering the private network. |
| **Network Access Privileges** | Permitting or blocking access to assets for specific roles, groups, or IP addresses | Reduces the risk of unauthorized users accessing the internal network. |
| **Password Policies** | Implementing NIST recommendations such as salting and hashing passwords | Prevents attackers from easily guessing passwords via scripts or brute force. |

---

## 📈 Hardening Recommendations & Effectiveness

### 1. Identity & Access Management (MFA & Password Policy)
* **Strategy:** Mandate **Multifactor Authentication (MFA)** and update **Password Policies** to align with NIST standards.
* **Effectiveness:** These measures protect against brute force attacks where attackers attempt to guess passwords manually or with scripts.
* **Implementation:** This is a "set up once and maintain" technique that provides 24/7 protection for all administrative and employee accounts.

### 2. Network Infrastructure (Firewall Maintenance & Port Filtering)
* **Strategy:** Execute **Firewall Maintenance** to check and update security configurations regularly and implement **Port Filtering**.
* **Effectiveness:** Port filtering controls network traffic and prevents potential attackers from entering a private network by blocking dangerous traffic before it passes through.
* **Implementation:** These rules should be updated in response to any events that allow abnormal traffic into the network to stay ahead of potential threats.

### 3. Monitoring (Network Log Analysis)
* **Strategy:** Configure **Network Log Analysis** using a SIEM tool to identify events of interest.
* **Effectiveness:** This alerts the security team to abnormal traffic patterns during or after a potential attack, allowing for faster response times.

---

## ✅ Conclusion
By addressing the identified vulnerabilities with these specific hardening tasks—MFA, Port Filtering, and NIST-aligned Password Policies—the organization will move from a reactive security posture to a proactive one. These tools ensure that even if one layer of defense is bypassed, multiple others remain to protect customer data.

---
**Source:** This risk assessment scenario and the list of network hardening tools were provided by the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
