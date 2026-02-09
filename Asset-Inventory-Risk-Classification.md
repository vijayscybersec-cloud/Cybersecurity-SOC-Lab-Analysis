# 📋 Home Office Asset Inventory & Risk Classification

## 📌 Executive Summary
Asset management is a foundational security practice. To protect a network, an analyst must first identify all connected devices and categorize them based on the sensitivity of the data they handle. In this project, I developed a comprehensive asset inventory for a home-based business to identify potential entry points and prioritize security resources.

---

## 🔍 Asset Inventory & Characteristics
I identified and cataloged devices connected to the network, evaluating their ownership and location to determine their threat profile.

| Asset | Network Access | Owner | Location | Sensitivity Level |
| :--- | :--- | :--- | :--- | :--- |
| **Network Router** | Continuous | ISP | On-premises | **Confidential** |
| **Desktop** | Occasional | Homeowner | On-premises | **Restricted** |
| **Guest Smartphone** | Occasional | Friend | On/Off-premises | **Internal-only** |

---

## 🛡️ Data Sensitivity Classification
I classified each asset using a four-tier sensitivity scale to ensure that security measures are proportional to the risk.

### 1. Restricted (High Sensitivity)
* **Example Asset:** Desktop Computer.
* **Justification:** Contains private PII (Personally Identifiable Information) and sensitive files like personal photos and business documents.
* **Access Designation:** Need-to-know basis only.

### 2. Confidential (Medium-High Sensitivity)
* **Example Asset:** Network Router.
* **Justification:** Serves as the primary gateway for all network traffic. Compromise could lead to total network interception.
* **Access Designation:** Limited to specific authorized users.

### 3. Internal-only (Medium Sensitivity)
* **Example Asset:** Guest Smartphone.
* **Justification:** While it connects to the home network, it does not store primary business data. However, it still requires basic authentication to prevent unauthorized lateral movement.
* **Access Designation:** Users on-premises.



---

## 🧠 Key Learning Outcomes
1. **Risk Prioritization:** Learned to differentiate between public information and restricted data to apply the Principle of Least Privilege.
2. **Attack Surface Mapping:** Identified that every connected device (including guest devices) represents a potential entry point that must be managed.
3. **Governance & Compliance:** Gained experience in documentation and inventory management, which is essential for meeting security audit requirements.

---
**Source:** This asset management and classification lab is based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
