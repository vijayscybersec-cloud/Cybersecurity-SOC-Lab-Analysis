# 🔍 Threat Intelligence Analysis: Malware Investigation via VirusTotal

## 📌 Executive Summary
I investigated a suspicious file alert involving a password-protected spreadsheet sent via a targeted phishing email. By analyzing the file's **SHA256 hash** through **VirusTotal**, I successfully identified the artifact as malicious and uncovered multiple Indicators of Compromise (IoCs). This report maps those findings to the **Pyramid of Pain** to evaluate the impact on the threat actor if these indicators are blocked.

---

## 🕵️ VirusTotal Investigation
**Artifact (SHA256):** `54e6ea47eb04634d3e87fd7787e2136ccfbcc80ade34f246a12cf93bab527f6b`

### Verdict: Malicious
The file is confirmed as **Malicious** based on the following findings:
* **Vendor Ratio:** A high percentage of security vendors (e.g., 50+/70) flagged this hash as a known Trojan or downloader.
* **Community Score:** The artifact received a significant negative community score, with reports of unauthorized executable files being created upon opening.
* **Behavioral Analysis:** Sandbox reports confirmed the execution of a malicious payload that established unauthorized network connections and modified system registries.

  ---

## 🔺 The Pyramid of Pain
I mapped the identified IoCs to the Pyramid of Pain to understand the difficulty for the attacker if these elements are neutralized.



### 1. Hash Values (Trivial)
* **IoC:** `MD5: 6961274534884279c1e792a549646944`
* **Analysis:** Blocking this hash is a basic first step, but it is "trivial" for an attacker to change the file's hash by altering a single bit of data.

### 2. IP Addresses (Easy)
* **IoC:** `185.224.128.83` (Identified in Contacted IP addresses)
* **Analysis:** Blocking this IP disrupts the malware's command-and-control (C2) communication, but attackers can "easily" spin up new proxy servers or use different IPs.

### 3. TTPs - Tactics, Techniques, and Procedures (Tough)
* **IoC:** MITRE ATT&CK® T1059 (Command and Scripting Interpreter) and T1204.002 (User Execution: Malicious File).
* **Analysis:** This is the most effective level of the pyramid. By identifying and blocking the *behavior* (e.g., blocking unsigned macros in spreadsheets), we make it "tough" or even "impossible" for the attacker to succeed, as they must reinvent their entire attack methodology.

---
**Source:** This malware analysis lab and the SHA256 artifact are based on the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
