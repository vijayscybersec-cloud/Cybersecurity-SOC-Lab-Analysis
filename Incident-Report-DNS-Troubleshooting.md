# 🛠️ Incident Report: Network Connectivity Troubleshooting

## 📝 Incident Summary
On January 30, 2026, at 13:24 PM, users reported an inability to access the website `www.yummyrecipesforme.com`. I performed a network analysis using `tcpdump` to identify the root cause of the service interruption.

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

## ✅ Resolution & Recommendations
1. **Immediate Action:** Escalated the issue to security engineers to restart the DNS service on the target server.
2. **Root Cause Analysis:** Investigating whether a recent firewall update blocked UDP Port 53.
3. **Prevention:** Recommend implementing an **Intrusion Detection System (IDS)** to alert when ICMP "unreachable" messages spike, as this can be a sign of a service failure or a DoS attack.
