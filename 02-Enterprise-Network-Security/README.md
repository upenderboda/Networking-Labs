# 🛡️ Enterprise Network Security Lab

<div align="center">

![Cisco Packet Tracer](https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?style=for-the-badge&logo=cisco&logoColor=white)
![Networking](https://img.shields.io/badge/Networking-VLANs-success?style=for-the-badge)
![Security](https://img.shields.io/badge/Security-ACL%20%7C%20SSH%20%7C%20Port%20Security-red?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**A secure enterprise network designed using Cisco Packet Tracer**

</div>

---

# 📖 Project Overview

This project demonstrates the design, implementation, and security hardening of a small enterprise network using **Cisco Packet Tracer**.

The network is divided into three departments using **Virtual Local Area Networks (VLANs)** and secured through industry-standard networking technologies including **Router-on-a-Stick (ROAS)**, **DHCP**, **SSH**, **Port Security**, and **Extended Access Control Lists (ACLs)**.

The primary objective is to simulate a real-world enterprise environment while applying networking fundamentals, segmentation, and access control.

---

# 🎯 Project Objectives

- Design an enterprise network for multiple departments
- Implement VLAN-based network segmentation
- Configure Inter-VLAN Routing
- Configure Dynamic Host Configuration Protocol (DHCP)
- Secure remote administration using SSH
- Prevent unauthorized device access using Port Security
- Restrict communication using Extended ACLs
- Verify network functionality through connectivity testing

---

# 🏗️ Network Topology

<p align="center">
<img src="Screenshots/01-Topology.png" width="900">
</p>

---

# 🖥️ Network Architecture

| VLAN | Department | Network Address | Subnet Mask | Default Gateway |
|------|------------|-----------------|-------------|-----------------|
| 10 | IT | 192.168.10.0/26 | 255.255.255.192 | 192.168.10.1 |
| 20 | Finance | 192.168.10.64/26 | 255.255.255.192 | 192.168.10.65 |
| 30 | Customer Service | 192.168.10.128/26 | 255.255.255.192 | 192.168.10.129 |

---

# 🏢 Enterprise Departments

## 🖥️ IT Department

- PCs
- Laptops
- Smartphones
- Tablets
- Network Printers
- Wireless Access Point

---

## 💰 Finance Department

- PCs
- Laptops
- Smartphones
- Tablets
- Network Printers
- Wireless Access Point

---

## 🎧 Customer Service Department

- PCs
- Laptops
- Smartphones
- Tablets
- Network Printers
- Wireless Access Point

---

# ⚙️ Technologies Used

- Cisco Packet Tracer
- Cisco IOS CLI
- VLAN Configuration
- IEEE 802.1Q Trunking
- Router-on-a-Stick (ROAS)
- DHCP
- SSH Version 2
- Port Security
- Extended ACLs

---

# 🔐 Security Features

| Security Feature | Status |
|------------------|--------|
| VLAN Segmentation | ✅ |
| Router-on-a-Stick | ✅ |
| DHCP | ✅ |
| SSH Version 2 | ✅ |
| Port Security | ✅ |
| Extended ACL | ✅ |

---

# 📷 Configuration Verification

---

## 1️⃣ VLAN Configuration

<p align="center">
<img src="Screenshots/02-VLAN-Brief.png" width="850">
</p>

✔ VLANs successfully created and assigned to switch ports.

---

## 2️⃣ Trunk Configuration

<p align="center">
<img src="Screenshots/03-Trunk-Configuration.png" width="850">
</p>

✔ IEEE 802.1Q trunk established between the switch and router.

---

## 3️⃣ Router Interface Configuration

<p align="center">
<img src="Screenshots/04-Router-IP-Interfaces.png" width="850">
</p>

✔ Router-on-a-Stick configured using subinterfaces.

---

## 4️⃣ DHCP Configuration

<p align="center">
<img src="Screenshots/05-DHCP-Binding.png" width="850">
</p>

✔ Dynamic IP addresses assigned successfully to all VLANs.

---

## 5️⃣ SSH Configuration

<p align="center">
<img src="Screenshots/06-SSH-Configuration.png" width="850">
</p>

✔ Secure remote management enabled using SSH Version 2.

---

## 6️⃣ Port Security

<p align="center">
<img src="Screenshots/07-Port-Security.png" width="850">
</p>

✔ Sticky MAC addressing enabled.

✔ Maximum MAC address = 1

✔ Violation mode = Shutdown

---

## 7️⃣ Access Control List (ACL)

<p align="center">
<img src="Screenshots/08-ACL-Verification.png" width="850">
</p>

✔ Extended ACL configured to prevent Customer Service devices from accessing the Finance VLAN.

---

## 8️⃣ Connectivity Test

### Allowed Communication

<p align="center">
<img src="Screenshots/09-Allowed-Ping.png" width="850">
</p>

✔ IT Department successfully communicates with Finance.

---

### Blocked Communication

<p align="center">
<img src="Screenshots/10-Blocked-Ping.png" width="850">
</p>

✔ Customer Service is denied access to Finance using an Extended ACL.

---

# 📂 Project Structure

```
02-Enterprise-Network-Security/
│
├── README.md
├── Enterprise-Network-Security.pkt
│
├── Configurations/
│   ├── Router-Running-Config.txt
│   └── Switch-Running-Config.txt
│
├── Documentation/
│   ├── IP-Addressing.md
│   ├── VLAN-Design.md
│   ├── Security-Policy.md
│   └── Troubleshooting.md
│
└── Screenshots/
    ├── 01-Topology.png
    ├── 02-VLAN-Brief.png
    ├── 03-Trunk-Configuration.png
    ├── 04-Router-IP-Interfaces.png
    ├── 05-DHCP-Binding.png
    ├── 06-SSH-Configuration.png
    ├── 07-Port-Security.png
    ├── 08-ACL-Verification.png
    ├── 09-Allowed-Ping.png
    └── 10-Blocked-Ping.png
```

---

# 🧪 Verification Commands

```bash
show vlan brief

show interfaces trunk

show ip interface brief

show ip dhcp binding

show ip dhcp pool

show access-lists

show port-security

show port-security interface fa0/3

show running-config
```

---

# 💡 Skills Demonstrated

- Enterprise Network Design
- VLAN Configuration
- IEEE 802.1Q Trunking
- Router-on-a-Stick (ROAS)
- Inter-VLAN Routing
- DHCP Configuration
- Secure Remote Management (SSH)
- Switch Port Security
- Extended Access Control Lists (ACLs)
- Cisco IOS CLI
- Layer 2 Switching
- Layer 3 Routing
- Network Troubleshooting

---

# 📚 What I Learned

This project provided practical experience in:

- Designing and implementing a segmented enterprise network.
- Configuring VLANs and trunk links for efficient traffic separation.
- Implementing Router-on-a-Stick for Inter-VLAN communication.
- Configuring DHCP for automated IP address allocation.
- Securing Cisco devices using SSH.
- Implementing Port Security to prevent unauthorized device access.
- Applying Extended ACLs to enforce communication policies.
- Verifying network functionality using Cisco IOS diagnostic commands.

---

# 🚀 Future Improvements

- OSPF Dynamic Routing
- NAT/PAT Configuration
- DNS Server
- Syslog Server
- SNMP Monitoring
- NTP Synchronization
- AAA Authentication
- Firewall Integration
- VPN Connectivity
- High Availability using HSRP

---

# 👨‍💻 Author

## **Boda Upender**

**Aspiring SOC Analyst | Networking | Cybersecurity | Cisco Packet Tracer | Python | SIEM**

---

## ⭐ Support

If you found this project helpful, consider giving this repository a ⭐ on GitHub.

It helps others discover the project and motivates continued learning and development.

---

<div align="center">

### Thank you for visiting this project!

**Happy Networking! 🚀**

</div>