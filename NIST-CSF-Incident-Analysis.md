# 🛡️ Incident Report Analysis: ICMP Flood (DoS) Attack

## 📝 Executive Summary
Recently, our multimedia organization experienced a **Denial of Service (DoS) attack** that lasted for two hours. The attack utilized a flood of ICMP packets to overwhelm the internal network, causing all network services to stop responding. This report analyzes the incident using the **NIST Cybersecurity Framework (CSF)** to improve our future security posture.

---

## 🔍 NIST CSF: Identify
In this stage, we determine the scope of the incident and the systems affected.

* **Attack Type:** ICMP Flood (Denial of Service).
* **Vulnerability:** An unconfigured firewall allowed unrestricted ICMP pings into the company's network.
* **Systems Impacted:** All internal network resources and web design/graphic design services were unavailable for two hours.
* **Goal:** Identify security gaps through regular audits of network devices and access privileges.

## 🛡️ NIST CSF: Protect
To further secure the organization’s assets, the following technical controls were implemented:

* **Firewall Rate Limiting:** A new rule was established to limit the rate of incoming ICMP packets to prevent overwhelming the CPU.
* **IP Verification:** Source IP address verification was enabled on the firewall to check for spoofed addresses.
* **Traffic Filtering:** An IDS/IPS system was deployed to filter out ICMP traffic based on suspicious characteristics.

---

## 👁️ NIST CSF: Detect
Improving monitoring capabilities ensures faster response times for future incidents.

* **Abnormal Traffic Detection:** Network monitoring software was installed to flag unusual spikes in traffic volume.
* **Firewall Logs:** Daily reviews of firewall logs will be conducted to identify unauthorized attempts from non-trusted IP addresses.
* **Access Tracking:** Implementation of software to track authorized versus unauthorized users and detect unusual account activity.


## ⚡ NIST CSF: Respond
A formal response plan has been created to contain and neutralize future incidents:

* **Containment:** Immediately block incoming ICMP packets at the firewall level when a flood is detected.
* **Neutralization:** Take all non-critical network services offline to preserve bandwidth for critical operations.
* **Analysis:** Use network logs and monitoring data to analyze the source and method of the attack for process improvement.

---

## 🔄 NIST CSF: Recover
Restoring the organization to normal operations involves the following steps:

* **Service Restoration:** Prioritize the restoration of critical network services first (e.g., client web design portals).
* **System Verification:** Test internal network resources to ensure they are fully responsive before bringing non-critical services back online.
* **Post-Incident Review:** Use the information gathered to update the "Identify" and "Protect" stages of the framework.


---
**Source:** This incident scenario and the NIST CSF analysis structure are provided by the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
