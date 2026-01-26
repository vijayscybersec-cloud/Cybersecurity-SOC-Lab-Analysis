# Cybersecurity-SOC-Lab-Analysis
Setting up a Controlled Environment for Traffic Analysis and Threat Detection.
# SOC Analyst Lab: Network Traffic & Threat Analysis

## 📌 Project Overview
The goal of this project was to set up a controlled SOC (Security Operations Center) environment to capture, analyze, and mitigate simulated network attacks. This project demonstrates my ability to monitor traffic, identify anomalies, and document security incidents professionally.

---

## 🛠️ Tools & Environment
* **Virtualization:** Oracle VirtualBox / VMware
* **OS:** Kali Linux (Attacker), Windows 10 (Target)
* **Analysis:** Wireshark & TCPDump
* **SIEM:** Splunk (for log ingestion)

---

## 🚀 Lab Implementation Steps

### Phase 1: Environment Setup
I configured a Private Host-Only Network to ensure the safety of the host machine while simulating attacks. 
- **Target IP:** 192.168.x.x
- **Attacker IP:** 192.168.x.x

### Phase 2: Simulating an Attack (e.g., SYN Flood / Port Scan)
Using Nmap, I performed a stealthy scan to identify open ports on the target Windows machine.
- **Command used:** `nmap -sS -T4 [Target IP]`

### Phase 3: Detection & Analysis
I used Wireshark to capture the handshake process. 
- **Finding:** I identified a high volume of TCP SYN packets without completion, indicating a potential Denial of Service (DoS) attempt.

---

## 📈 Visual Documentation
> **[HEADING: INSERT SCREENSHOT OF YOUR WIRESHARK CAPTURE HERE]**
> *Note: I captured the 3-way handshake and filtered for 'tcp.flags.syn == 1'.*

---

## 🧠 Key Learning Outcomes
1. **Network Fundamentals:** Deepened understanding of the OSI Model and TCP/IP stack.
2. **Log Analysis:** Learned how to distinguish between normal user traffic and malicious scanning.
3. **Incident Reporting:** Developed a workflow for documenting security events for executive review.

---

## 🔗 How to Replicate
1. Download the [config file/script name] provided in this repo.
2. Run the lab setup in VirtualBox...
