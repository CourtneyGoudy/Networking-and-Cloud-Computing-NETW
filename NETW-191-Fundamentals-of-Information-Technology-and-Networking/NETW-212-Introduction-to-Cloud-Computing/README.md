# NETW 212 — Introduction to Cloud Computing

### Course & Lab Overview
During **NETW 212 (Introduction to Cloud Computing)** at **DeVry University** (96/100 Post-Assessment), I completed hands-on labs covering server virtualization, Ubuntu Linux administration, SSH/RSA key authentication, AWS Virtual Private Cloud (VPC) network architecture, asymmetric cryptography, redundant storage (RAID 5 and NFS), and AI-assisted network traffic monitoring.

---

### Platforms, Tools & Cloud Concepts Practiced
- **Virtualization & Operating Systems:** Microsoft Hyper-V (compatibility verification, virtual switches, NAT virtual networking) and Ubuntu Linux (guest installation and remote SSH administration)
- **Cloud Platforms & Architecture:** Amazon Web Services (AWS VPC, public/private subnets, Availability Zones, Route Tables, Internet Gateway, NAT Gateway, Elastic IP, Security Groups, Network ACLs) and Microsoft Azure cloud deployment concepts
- **Cloud Service & Deployment Models:** IaaS, PaaS, SaaS, Public, Private, Hybrid, and Community Cloud, Shared Responsibility Model, Horizontal/Vertical Scaling, Elasticity, and Right-Sizing
- **Cryptography & Access Security:** OpenSSL, Kleopatra (public/private key pair generation), RSA authentication, SSH, HTTPS, VPNs, Identity Federation, Single Sign-On (SSO), and Vulnerability Scanning
- **Storage & Monitoring:** RAID, RAID 5, Network File System (NFS) datastores, Network Traffic Monitoring, and Real-Time AI-Assisted Traffic Analysis

---

### Cloud Architecture Design: Multi-Subnet AWS VPC (`10.0.0.0/16`)
Designed a segmented AWS cloud network separating internet-facing resources from protected internal workloads across multiple subnets:

| Network Component | CIDR / Target | Access Tier & Purpose |
| :--- | :--- | :--- |
| **VPC Network** | `10.0.0.0/16` | Isolated cloud network (`local` internal routing) |
| **Public Subnet A** | `10.0.1.0/24` | Public tier; hosts internet-facing resources and NAT Gateway (with Elastic IP) |
| **Public Subnet B** | `10.0.2.0/24` | Public tier for multi-Availability Zone redundancy |
| **Private Subnet A** | `10.0.11.0/24` | Private tier for internal workloads; no direct inbound internet access |
| **Private Subnet B** | `10.0.12.0/24` | Private tier for multi-Availability Zone redundancy |

- **Public Route Table:** `0.0.0.0/0` $\rightarrow$ **Internet Gateway** (supports inbound/outbound internet traffic for public-facing services).
- **Private Route Table:** `0.0.0.0/0` $\rightarrow$ **NAT Gateway** in Public Subnet A (allows private instances to initiate outbound connections for OS patches and updates without exposing public IP addresses).
- **Security & Resilience Notes:** Documented that a NAT Gateway is not a firewall—stateful **Security Groups** and stateless **Network ACLs** are still required to filter traffic, and production environments deploy one NAT Gateway per Availability Zone for high availability. *(Architecture design exercise using example resource identifiers rather than a live AWS production account.)*

---

### Completed Hands-On Labs
1. **Hyper-V Virtualization & Virtual Networking:** Verified hardware compatibility, enabled Hyper-V on Windows, created virtual network switches, and configured a NAT virtual network.
2. **Ubuntu Linux & Secure Remote Administration:** Installed Ubuntu Linux as a virtual guest, generated an RSA public/private key pair, and established an encrypted SSH session.
3. **Public-Key Cryptography (Kleopatra & OpenSSL):** Generated asymmetric public/private encryption key pairs using both Kleopatra and OpenSSL.
4. **Enterprise Cloud Storage (RAID, RAID 5 & NFS):** Configured fault-tolerant RAID/RAID 5 storage arrays and connected a shared Network File System (NFS) datastore.
5. **Network & AI-Assisted Traffic Monitoring:** Monitored network traffic patterns and evaluated how real-time AI analysis supports anomaly and threat detection.

---

### Key Takeaways & Troubleshooting
- **Public vs. Private Cloud Routing:** Learned how separating route tables, Internet Gateways, and NAT Gateways allows private cloud servers to download updates safely without accepting unsolicited inbound internet connections.
- **Defense-in-Depth in the Cloud:** Reinforced how the Shared Responsibility Model requires customers to lock down their own subnets, firewall rules (Security Groups/NACLs), and SSH/RSA keys.
- **Fault-Tolerant Storage & Architecture Tradeoffs:** Balanced cost, scalability, availability, and security across RAID 5 storage, cloud pricing models, and multi-AZ design.
- **Network vs. Configuration Troubleshooting:** Diagnosed connection bottlenecks during virtual machine labs by testing an alternate hotspot connection, isolating network latency from local VM configuration steps to complete the Ubuntu, NAT, RSA, and SSH labs.
