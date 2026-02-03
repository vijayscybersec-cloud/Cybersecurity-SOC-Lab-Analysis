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

## 🛠️ Proposed Network Hardening Tools
To address these gaps, I recommend implementing the following industry-standard tools and practices:

* **Firewalls:** To monitor and filter network traffic based on configured security rules.
* **Intrusion Detection Systems (IDS):** To identify and alert on suspicious activity or known attack patterns.
* **Encryption:** To protect data in transit and at rest, ensuring that even if data is intercepted, it remains unreadable.
* **Network Access Concept (Least Privilege):** Implementing strict permissions so users only access what is necessary for their role.

## 📈 Hardening Recommendations & Effectiveness

### 1. Firewall Rule Configuration (Port Filtering)
* **Action:** Configure firewall rules to block all non-essential ports and filter traffic coming in and out of the network.
* **Effectiveness:** This prevents unauthorized access to sensitive internal services and stops malware from "calling home" to an attacker's server. 
* **Frequency:** Firewall logs should be reviewed daily, and rule sets should be audited monthly to remove outdated permissions.



### 2. Identity and Access Management (MFA & Password Policy)
* **Action:** Force a global password reset, prohibit password sharing, and mandate Multi-Factor Authentication (MFA) for all accounts.
* **Effectiveness:** MFA provides a critical second layer of defense. Even if an attacker steals a password, they cannot gain access without the second factor (e.g., an authenticator app code).
* **Frequency:** Password complexity requirements are enforced 24/7; MFA is required at every login attempt.



[Image of multi-factor authentication process]


---

## ✅ Conclusion
By addressing these four core vulnerabilities through a combination of technical controls (Firewalls/IDS) and administrative policies (MFA/Password Hygiene), the organization can significantly reduce its attack surface and protect customer data from future breaches.

---
**Source:** This risk assessment scenario and hardening tool list are provided by the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
