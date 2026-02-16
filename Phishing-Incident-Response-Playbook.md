# 🎣 Incident Response: Phishing Alert & Playbook Execution

## 📌 Executive Summary
I acted as a Level 1 SOC Analyst to respond to a suspicious email alert. Following the organization's **Phishing Playbook**, I evaluated the alert's legitimacy, analyzed the sender's details, and followed a structured flowchart to determine if escalation was required. This project demonstrates my ability to handle alert tickets within a professional workflow.

---

## 🔍 Step 1: Alert Evaluation (The 5 W's)
I analyzed the **Alert Ticket (ID: A-2703)** to understand the scope of the threat:

* **Who:** An external sender (`76tguyhh6tgftrt7tg.su`) claiming to be "Clyde West".
* **What:** A possible phishing attempt featuring a password-protected malicious attachment (`bfsvc.exe`).
* **When:** July 20, 2022, at 09:30:14 AM.
* **Where:** Target was the HR department (`hr@inergy.com`).
* **Why:** To trick the HR staff into bypass scanning by providing a password for a malicious executable disguised as a resume.

---

## 🛠️ Step 2: Playbook Workflow
I followed the **Phishing Playbook Version 1.0** to ensure all investigative steps were completed.



### Investigation Findings:
1. **Severity:** Marked as **Medium**, which meets the threshold for detailed investigation.
2. **Inconsistency:** The sender's name ("Def Communications") and email address did not match the persona of a job applicant, a common phishing indicator.
3. **Malicious Artifact:** The attachment `bfsvc.exe` was previously verified as malicious via its SHA256 hash in threat intelligence tools.

### 📉 Resolution & Escalation
* **Ticket Status:** **Escalated**.
* **Comments:** I escalated this ticket to a Level 2 Analyst because the attachment has been confirmed as malicious malware. The sender's address is highly suspicious, and the use of a password-protected `.exe` file is a clear attempt to bypass automated email security filters.

---
**Source:** This incident response lab and playbook materials are based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
