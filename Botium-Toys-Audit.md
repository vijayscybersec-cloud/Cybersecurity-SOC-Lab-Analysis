# Internal IT Audit: Botium Toys 🧸

## 📌 Scenario Overview
Botium Toys is a growing retailer needing a security audit to ensure international growth is safe and compliant with GDPR and PCI DSS regulations.

---

## 📊 Controls Assessment Checklist
| Control | In Place? | Recommendation |
| :--- | :--- | :--- |
| **Least Privilege** | ❌ No | Restrict data access so employees only see what they need. |
| **Encryption** | ❌ No | Encrypt the database to protect credit card information. |
| **Disaster Recovery** | ❌ No | Create a backup plan for critical data immediately. |
| **IDS (Intrusion Detection)** | ❌ No | Install an IDS to monitor for network threats. |
| **Firewall** | ✅ Yes | Keep current rules; continue regular monitoring. |
| **Antivirus** | ✅ Yes | Ensure software is updated on all laptops. |
| **Physical Locks/CCTV** | ✅ Yes | No changes needed; physical security is strong. |

---

## 📜 Compliance Mapping
* **PCI DSS:** Currently non-compliant. **Action:** Must implement encryption for stored cardholder data.
* **GDPR:** Currently non-compliant. **Action:** Must secure E.U. customer PII to avoid heavy fines.
* **SOC Type 1/2:** Needs improvement on data confidentiality and user access policies.

---

## 💡 Top 3 Strategic Recommendations
1. **Encrypt the Database:** This is the highest priority to meet legal standards.
2. **Implement RBAC:** Use Role-Based Access Control to enforce "Least Privilege."
3. **Set up Backups:** Ensure business continuity with a disaster recovery plan.
