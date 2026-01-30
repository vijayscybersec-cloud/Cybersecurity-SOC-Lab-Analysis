# 🛠️ Incident Report: Network Connectivity Troubleshooting

## 📝 Incident Summary
As part of a technical lab in the Google Cybersecurity Certificate program, I analyzed a simulated network outage for the website www.yummyrecipesforme.com. Using tcpdump logs, I investigated the root cause of a service interruption affecting external users.

---

## 🔍 Technical Analysis (tcpdump)
Upon analysis of the packet capture, I observed the following:
- **Source IP:** 192.51.100.15 (Client)
- **Destination IP:** 203.0.113.2 (DNS Server)
- **Protocol:** UDP (Query) / ICMP (Error Response)
- **Error Received:** `udp port 53 unreachable.`

### Findings:
The browser attempted to resolve the domain name via a DNS A-record request. However, the DNS server responded with an **ICMP Destination Unreachable** message. This indicates that while the server was reachable, the DNS service on Port 53 was not active or was being blocked.

---

## 📈 Visual Evidence
![tcpdump Log Analysis](image_805052.png)

*Note: The log shows repeated ICMP error packets, confirming a persistent service outage.*

---

## 📝 Formal Incident Report

### Part 1: Summary of the Problem
* **Protocol Findings:** The UDP protocol reveals that the client (192.51.100.15) attempted to send a DNS query to the server (203.0.113.2).
* **Error Analysis:** The network analysis results show that the ICMP echo reply returned the error message: `udp port 53 unreachable`.
* **Port Usage:** Port 53 is used for DNS (Domain Name System) services.
* **Primary Issue:** The DNS service was unavailable or blocked, preventing the website domain from resolving to an IP address.

### Part 2: Incident Analysis
* **Timestamp:** 13:24:32 (1:24 PM).
* **Discovery:** The IT team became aware through customer reports of "destination port unreachable" errors.
* **Investigation Steps:** The IT department confirmed the error by visiting the site and then used `tcpdump` to inspect traffic logs.
* **Key Findings:** Multiple ICMP "unreachable" responses were received from the DNS server, confirming a service outage.
* **Root Cause:** No service was listening on Port 53, likely due to a service crash or firewall misconfiguration.

---

## ✅ Resolution & Recommendations
1. **Immediate Action:** Escalated the issue to security engineers to restart the DNS service on the target server.
2. **Root Cause Analysis:** Investigating whether a recent firewall update blocked UDP Port 53.
3. **Prevention:** Recommend implementing an **Intrusion Detection System (IDS)** to alert when ICMP "unreachable" messages spike, as this can be a sign of a service failure or a DoS attack.

---

**Source:** This incident scenario and log data are provided by the **Google Cybersecurity Professional Certificate** curriculum on Coursera.
