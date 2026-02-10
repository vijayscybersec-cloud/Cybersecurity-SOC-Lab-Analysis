# 🔍 Security Analysis: USB Baiting & Social Engineering

## 📌 Executive Summary
I investigated a potential **USB Baiting** incident after discovering a flash drive with the organization's logo in the company parking lot. To prevent potential malware from infecting the hospital's network, I utilized a **Virtual Machine (VM)** to safely sandbox and inspect the device's contents. This report analyzes the risks associated with the discovered data and proposes controls to mitigate physical social engineering threats.

---

## 🔍 Forensic Inspection (Virtual Environment)
The USB drive was plugged into a standalone workstation running virtualization software to isolate it from the internal network.



### 📂 Device Contents
The drive appears to belong to a Human Resources (HR) Manager and contains a high-risk mixture of personal and professional data:
* **Personal Data:** Folders containing family and pet photographs.
* **Professional Data:** A new hire letter and an employee shift schedule.
* **PII Risk:** The drive contains **Personally Identifiable Information (PII)** that could compromise both the owner and the organization.

---

## 🧠 Attacker Mindset & Social Engineering
From a security perspective, this device represents a significant **Social Engineering** risk. 

An attacker could use the employee shift schedule to plan physical unauthorized access or time a digital attack when key personnel are off-duty. Furthermore, the personal photos could be used to craft highly convincing **Spear Phishing** emails or to blackmail the employee, providing the attacker with a "backdoor" into the hospital’s sensitive systems.

---

## 🛡️ Risk Analysis & Proposed Mitigations
USB baiting relies on curiosity to bypass digital defenses. I recommend the following controls to mitigate these risks:

* **Technical Control:** Implement **USB Port Blocking** software on all company workstations to prevent unauthorized mass storage devices from being mounted.
* **Operational Control (Policy):** Establish a strict policy prohibiting the mixing of personal and business data on the same device. Use encrypted, company-issued drives for business needs.
* **Managerial Control (Awareness):** Conduct regular **Social Engineering Awareness Training** to teach employees never to plug in found devices and to report them to the security team immediately.



---
**Source:** This USB baiting exercise is based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
