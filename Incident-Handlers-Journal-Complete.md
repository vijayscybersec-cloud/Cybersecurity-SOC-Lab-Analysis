# 📓 Complete Incident Handler's Journal: Lifecycle & Tool Analysis

## 📌 Executive Summary
This journal serves as a comprehensive record of my technical training in incident detection and response. It documents my hands-on experience with various security tools and my ability to analyze security events through every phase of the **NIST Incident Response Lifecycle**.

---

## 🔄 NIST Incident Response Lifecycle
Throughout this journal, I categorize activities into the four NIST phases to demonstrate strategic alignment with industry standards:



1.  **Preparation:** Establishing tools and playbooks before an incident occurs.
2.  **Detection & Analysis:** Identifying signs of a breach and determining its scope.
3.  **Containment, Eradication, & Recovery:** Neutralizing threats and restoring systems.
4.  **Post-Incident Activity:** Learning from the event to improve future defenses.


---

## 🕒 Featured Journal Entries

### Entry #1: Healthcare Ransomware (Detection & Analysis)
* **The 5 W's:** Analyzed a phishing-led ransomware attack on a U.S. health clinic that encrypted critical patient data.
* **Tools:** Phishing Playbooks, Email Headers.
* **Outcome:** Identified the attack vector as a malicious attachment and recommended system isolation.

### Entry #2: Malware Investigation (Detection & Analysis)
* **The 5 W's:** Investigated a suspicious SHA256 file hash retrieved from an employee workstation.
* **Tools:** **VirusTotal**, **Pyramid of Pain**.
* **Outcome:** Verified the artifact as a malicious Trojan and identified related C2 IP addresses to block at the firewall.

### Entry #3: Network Traffic Baseline (Preparation)
* **Description:** Captured and analyzed local network traffic to establish a baseline of "normal" DNS activity.
* **Tools:** **Wireshark**, **tcpdump**.
* **Outcome:** Mastered the use of display filters to isolate UDP Port 53 traffic and verify authorized DNS resolvers.

### Entry #4: SIEM Log Querying (Detection & Analysis)
* **Description:** Performed advanced queries to detect after-hours login attempts and unauthorized access patterns.
* **Tools:** **SQL**, **Splunk**, **Chronicle**.
* **Outcome:** Created filtered datasets to isolate failed logins, reducing "noise" for the security team.

---

## 🧠 Reflections & Notes
* **Challenges:** Mastering the syntax of packet filters in Wireshark was initially challenging, but repeated practice with live captures helped me understand the relationship between protocols and ports.
* **Growth:** My understanding has shifted from seeing security as just "blocking hackers" to seeing it as a structured lifecycle of identification, protection, and continuous improvement.
* **Favorite Tool:** I most enjoyed working with **SQL** and **SIEM tools**, as they provide the power to turn millions of raw logs into actionable security intelligence.

---
**Source:** This journal is a culmination of activities from the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
