# NETW 191 — Fundamentals of Information Technology and Networking

### Course & Lab Overview
During **NETW 191 (Fundamentals of Information Technology and Networking)** at **DeVry University**, I completed 7 graded hands-on networking and cloud labs (earning 280/280 points) alongside enterprise network design and troubleshooting assessments. My coursework focused on IPv4 addressing, packet structure, DNS record inspection, virtual switching, cloud networking in AWS, VLAN segmentation, and defensive honeypot security.

---

### Tools, Protocols & Commands Practiced
- **Platforms & Environments:** uCertify Simulated Networking Labs, Windows PowerShell, and Amazon Web Services (AWS)
- **Networking Protocols & Concepts:** TCP/IP, IPv4, HTTP/HTTPS, DNS, DHCP, SSH, ICMP, Virtual Local Area Networks (VLANs), Quality of Service (QoS), Routing, and Network Segmentation
- **DNS & Connectivity Diagnostic Commands:**
  - `nslookup www.wiley.com` — Query standard DNS address resolution
  - `nslookup -q=cname www.wiley.com` — Inspect canonical name (alias) DNS records
  - `nslookup -q=mx wiley.com` — Identify mail exchange (MX) servers for a domain
  - `nslookup -q=mx wiley.com >> sample.txt` — Redirect command-line DNS query output into a text file
  - `ping`, `tracert`, and `traceroute` — Connectivity and network path verification concepts

---

### Completed Hands-On Labs (280/280 — 100%)
1. **Viewing the IPv4 Header (Module 1):** Examined IPv4 packet header fields to understand how source/destination addressing and protocol metadata route traffic across networks.
2. **Understanding HTTP/HTTPS (Module 2):** Explored standard vs. encrypted web communication protocols and client-server request behavior.
3. **Configuring an IPv4 Address (Module 2):** Configured host IPv4 addressing parameters to establish valid network communication.
4. **Creating a VPC in AWS (Module 3):** Built an isolated Virtual Private Cloud (VPC) environment in Amazon Web Services to practice cloud network architecture.
5. **Creating a Virtual Switch (Module 4):** Configured virtual switching to connect virtual network interfaces within a simulated infrastructure.
6. **Examining DNS Entries (Module 5):** Used Windows PowerShell and `nslookup` queries to inspect A, CNAME, and MX DNS records and export results.
7. **Using a Honeypot (Module 6):** Deployed and examined a decoy honeypot system to observe how security teams detect and monitor unauthorized network activity.

---

### Enterprise VLAN & Troubleshooting Scenario Practiced
In an applied troubleshooting assessment, I analyzed root causes across a segmented multi-VLAN enterprise network:

| VLAN ID | Network Segment Function |
| :--- | :--- |
| **VLAN 10** | Corporate End Users |
| **VLAN 20** | VoIP / IP Phones |
| **VLAN 30** | Corporate Wi-Fi |
| **VLAN 50** | Internal Servers & Shared Services |
| **VLAN 60** | Network Infrastructure Management |

- **Scenarios Investigated:** Internal server reachability failures, intermittent corporate Wi-Fi connectivity, blocked administrator SSH access to switches, and IP phone registration drops during peak traffic.
- **Root-Cause Factors Analyzed:** DHCP scope/lease issues, DNS resolution failures, firewall access rules, VLAN tagging/trunking misconfigurations, and Quality of Service (QoS) voice prioritization.

---

### Key Takeaways & IT Support Relevance
- **Structured Network Diagnostics:** Learned how to isolate connectivity issues layer-by-layer—checking IP configuration, DHCP, DNS resolution, firewall rules, and VLAN assignments before escalating.
- **Segmented Network Architecture:** Understood why businesses separate user traffic, voice (VoIP), wireless, servers, and management interfaces into dedicated VLANs for performance and security.
- **Cloud & Security Integration:** Connected foundational on-premises networking concepts directly to cloud VPC design and active threat detection using honeypots.
