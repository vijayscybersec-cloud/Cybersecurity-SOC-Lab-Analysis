# 📑 Post-Incident Analysis: E-commerce Data Breach & Final Report

## 📌 Executive Summary
I performed a comprehensive review of a final incident report following a major security breach at a mid-sized retail organization. The incident involved the unauthorized access and exfiltration of approximately 50,000 customer PII and financial records via a web application vulnerability. This project demonstrates my ability to analyze the full lifecycle of an incident and evaluate long-term remediation strategies.

---

## 🕒 Incident Timeline
The following timeline outlines the key events from initial threat to incident closure:
* **Dec 22, 2022:** Initial extortion email received; attacker demanded $25,000 in cryptocurrency.
* **Dec 28, 2022:** Second email received with a sample of stolen data; demand increased to $50,000.
* **Dec 28, 2022:** Security team notified; investigation and containment phase began.
* **Dec 31, 2022:** Scope of theft determined and investigation concluded.

---

## 🔍 Investigation & Root Cause
The security team identified the following technical failures during the investigation:
* **Root Cause:** A vulnerability in the e-commerce web application allowed for a **Forced Browsing** attack.
* **Exploit Method:** The attacker modified order numbers in the URL string of purchase confirmation pages to access other customers' data without authorization.
* **Evidence:** Web server access logs showed an exceptionally high volume of sequentially listed customer orders from a single source.

---

## 🛠️ Response & Future Recommendations
To remediate the vulnerability and restore customer trust, the organization took the following actions:

### Immediate Response:
* Disclosed the breach to customers in collaboration with Public Relations.
* Offered free identity protection services to all affected customers.

### Long-Term Recommendations (Post-Incident):
1. **Vulnerability Management:** Implement routine vulnerability scans and penetration testing to identify "Forced Browsing" and other OWASP Top 10 risks.
2. **Access Control (Allowlisting):** Implement URL allowlisting to automatically block requests outside of specified valid ranges.
3. **Robust Authentication:** Ensure all content containing PII requires a valid, authenticated session before access is granted.



---
**Source:** This final report analysis is based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
