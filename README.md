# 🛡️ Cybersecurity & SOC Analyst Portfolio
Welcome to my technical portfolio. This repository serves as a professional showcase of my transition from **US IT Recruitment** and a **BCA background** into **Security Operations**. Here, I demonstrate my proficiency in network traffic analysis, incident response, system administration, and proactive defense using the **NIST Cybersecurity Framework (CSF)**.

---

## 🚀 Incident Reports & Security Audits
Each project below represents a real-world scenario analyzed during my professional certification training.

### 🏛️ Governance & Risk Management
* **[Internal Security Audit: Botium Toys](./Botium-Toys-Audit.md)**
    * Performed a comprehensive security audit of a fictional toy company.
    * Mapped assets and vulnerabilities to the **NIST CSF** to identify critical gaps in physical and digital security.
* **[Home Office Asset Inventory & Classification](./Asset-Inventory-Risk-Classification.md)**
    * Created a detailed inventory of network assets and classified them by sensitivity (Restricted, Confidential, Internal).
    * Evaluated risk factors such as network access frequency and physical location to prioritize security controls.
* **[Bank Risk Assessment & Register](./Risk-Assessment-Bank-Register.md)**
    * Evaluated a commercial bank's operational environment to identify and score potential security risks.
    * Calculated priority scores (Risk = Likelihood x Impact) to help stakeholders allocate resources to the most critical vulnerabilities.
* **[Data Leak Prevention: NIST AC-6 Analysis](./Data-Leak-Prevention-NIST-AC6.md)**
    * Analyzed a real-world data leak scenario involving unauthorized folder sharing and human error.
    * Applied **NIST SP 800-53: AC-6** controls to recommend Role-Based Access Control (RBAC) and automated access revocation.

### 🕵️ Network Traffic Analysis (Incident Response)
* **[DNS Troubleshooting: Port Unreachable](./Incident-Report-DNS-Troubleshooting.md)**
    * Investigated connectivity issues for `yummyrecipesforme.com` using `tcpdump`.
    * Identified a service failure on **UDP Port 53** via ICMP error analysis.
* **[DDoS Detection: TCP SYN Flood](./Incident-Report-SYN-Flood-Analysis.md)**
    * Analyzed packet captures to identify an incomplete TCP three-way handshake pattern.
    * Documented how "half-open" connections were used to exhaust server resources.
* **[Web Compromise: Brute Force & Malware](./Incident-Report-Brute-Force-Malware.md)**
    * Analyzed a multi-stage attack involving a default password exploit and a malicious JavaScript redirect.
    * Traced browser redirection from a legitimate site to a malware-hosting domain in network logs.

### 🛡️ Defensive Hardening & Strategy
* **[Security Risk Assessment & Hardening Plan](./Security-Risk-Assessment-Hardening.md)**
    * Developed a proactive hardening roadmap for a social media organization.
    * Proposed technical controls including **MFA**, **Port Filtering**, and **Firewall Maintenance**.
* **[NIST CSF Lifecycle Analysis: DoS Event](./NIST-CSF-Incident-Analysis.md)**
    * Applied the "Identify, Protect, Detect, Respond, and Recover" lifecycle to a two-hour ICMP flood incident.
    * Established long-term strategies for rate limiting and IDS/IPS integration.

### 🐧 System Administration & IAM
* **[Linux File Permissions & Hardening](./Linux-Permissions-Security-Lab.md)**
    * Managed user and group access levels for sensitive directories using `chmod` and `chown`.
    * Applied the Principle of Least Privilege to secure internal project files and directories.

### 📊 Database Security & Logging
* **[SQL Security Filters & Querying](./SQL-Security-Filters-Lab.md)**
    * Used SQL to investigate after-hours failed login attempts and suspicious activity.
    * Applied logical operators (`AND`, `OR`, `NOT`) and pattern matching (`LIKE`) to filter log data.

---

## 🛠️ Technical Toolkit
* **Analysis Tools:** Wireshark, `tcpdump`, Packet Inspection.
* **Operating Systems:** Linux (Ubuntu/Debian), Windows.
* **Databases:** SQL (PostgreSQL, BigQuery filters).
* **Frameworks:** NIST Cybersecurity Framework (CSF), NIST SP 800-53.
* **Network Security:** Firewalls, IDS/IPS, Multi-Factor Authentication (MFA), Port Filtering.
* **Protocols:** TCP/IP, DNS (UDP 53), HTTP/HTTPS, ICMP.

---

## 🧠 Core Competencies
1.  **Forensic Investigation:** Skilled in using SQL to query database logs for suspicious login patterns and after-hours activity.
2.  **Identity & Access Management (IAM):** Proficient in managing Linux permissions and implementing MFA to ensure only authorized users access sensitive data.
3.  **Packet Inspection:** Ability to isolate "needles in a haystack" using display filters to detect anomalies like DNS Tunneling.
4.  **Incident Documentation:** Proficient in writing technical reports that bridge the gap between raw data and business impact.

---

## 🔗 Connect with Me
I am seeking a **Junior SOC Analyst** or **Security Analyst** role where I can apply my analytical mindset and technical training to protect organizational assets.

* **Background:** BCA Graduate (Bangalore) | Former US IT Recruiter (2.5 Years)
* **Current Focus:** CompTIA Security+ & Google Cybersecurity Professional Certificate
