# 🛡️ Incident Analysis: Data Leak Prevention & Least Privilege

## 📌 Executive Summary
I investigated a data leak at an educational technology company where confidential business plans were accidentally shared on social media. The incident stemmed from a failure to observe the **Principle of Least Privilege (PoLP)** during a sales meeting, resulting in unauthorized external access to sensitive customer analytics and internal product files.

---

## 🔍 Incident Investigation
### Root Cause Analysis (The Issue)
The leak was caused by a combination of managerial oversight and employee error:
1. **Managerial Failure:** A manager granted broad folder access but failed to revoke permissions after the meeting.
2. **Technical Overshare:** A sales representative accidentally shared a link to the entire internal folder instead of just the intended marketing materials.
3. **Lack of Controls:** The absence of automated access expiration or restricted sharing permissions allowed the internal data to be publicly posted by a third party.

---

## 📖 Framework Review: NIST SP 800-53 (AC-6)
To address this, I analyzed **NIST SP 800-53: AC-6**, which focuses on **Least Privilege**. This standard ensures that users are only provided the minimum access required to complete their specific business functions, preventing users from operating at higher privilege levels than necessary.

---

## 🛠️ Security Recommendations (Control Enhancements)
Based on the NIST SP 800-53 guidelines, I recommend the following enhancements to prevent future leaks:

1. **Role-Based Access Control (RBAC):** Restrict access to sensitive resources based specifically on the user's role. A sales representative should not have "Owner" or "Manager" level permissions for internal strategy folders.
2. **Automated Access Revocation:** Implement a system that automatically revokes or expires access to sensitive information after a set period (e.g., 24 hours) or once a meeting concludes.
3. **Regular Privilege Audits:** Conduct monthly reviews of shared folder permissions to identify and remove "permission creep".

---

## ✅ Justification
Implementing these **AC-6 control enhancements** reduces the "human error" factor. By automating the revocation of access, we ensure that folders do not remain open indefinitely if a manager forgets to manualy unshare them. Role-based restrictions further ensure that even if a link is shared accidentally, the recipient's ability to view or re-post the data is limited by pre-defined security policies.

---
**Source:** This data leak scenario and the NIST SP 800-53 reference are based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
