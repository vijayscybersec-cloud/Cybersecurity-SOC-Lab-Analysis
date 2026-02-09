# 🏦 Risk Assessment: Commercial Bank Risk Register

## 📌 Executive Summary
As part of a new cybersecurity team at a commercial bank, I conducted a risk assessment to evaluate vulnerabilities threatening business operations. By developing a **Risk Register**, I identified the likelihood and severity of various threats, allowing the organization to prioritize resources effectively using the formula: `Likelihood x Severity = Risk Score`.

---

## 🏢 Operational Environment
The assessment considered the following environmental factors:
* **Location:** Coastal area (low crime, high natural disaster risk).
* **Workforce:** 100 on-premise and 20 remote employees.
* **Regulation:** Strict Federal Reserve requirements for securing data and liquid funds.
* **Scope:** 2,000 individual and 200 commercial accounts.

### 🕵️ Security Event Possibility
In this environment, security events are likely due to the high volume of remote access points and the high value of the assets (funds). Malicious actors may target employees via phishing (BEC), while environmental hazards like hurricanes pose a significant threat to physical supply chains.

---

## 📊 Risk Register & Priority Scores
I evaluated five primary risks using a 1-3 scale for Likelihood and Severity.

| Asset | Risk | Description | Likelihood | Severity | Priority (Risk) |
| :--- | :--- | :--- | :---: | :---: | :---: |
| **Funds** | Financial Records Leak | Database server of backed-up data is publicly accessible. | 2 | 3 | **6** |
| **Funds** | Business Email Compromise | An employee is tricked into sharing confidential info. | 3 | 2 | **6** |
| **Funds** | Compromised User Database | Customer data is poorly encrypted and exposed. | 2 | 3 | **6** |
| **Funds** | Supply Chain Disruption | Coastal hurricanes causing delivery delays of cash. | 1 | 3 | **3** |
| **Funds** | Theft | The bank's safe is left unlocked during business. | 1 | 3 | **3** |

---

## 📈 Priority Analysis

Based on the scores, the bank should prioritize **Financial Records Leaks**, **Business Email Compromise**, and **User Database Security**. 
* **High Priority (Score 6):** These events are moderately to highly likely and would cause catastrophic financial or reputational damage.
* **Medium Priority (Score 3):** While the severity is high (e.g., a hurricane or safe theft), the likelihood is low due to the bank's location in a low-crime area and the rarity of extreme weather.

---
**Source:** This risk register activity is based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
