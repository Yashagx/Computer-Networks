🏨 Hotel Management System Network – Cisco Packet Tracer Simulation
📘 A Case Study Report for 21CSC302J – Computer Networks

SRM Institute of Science and Technology, Kattankulathur

📋 Project Overview

This project presents a complete network design and simulation of a Hotel Management System implemented using Cisco Packet Tracer. It demonstrates how an integrated digital infrastructure can streamline communication across hotel departments spread over multiple floors.

The network uses a three-layer hierarchical model — Core, Distribution, and Access — to ensure scalability, security, and performance.

🎯 Objectives

Design a multi-floor hierarchical network connecting all hotel departments.

Segment the network using VLANs for data isolation and optimized performance.

Implement DHCP, NAT/PAT, and OSPF for dynamic routing and IP management.

Configure SSH, ACLs, and Port Security for robust security.

Validate performance using simulation in Cisco Packet Tracer.

🧩 Network Architecture
🔹 Layers:

Core Layer: 3 × Cisco 2911 Routers (inter-floor OSPF routing, redundancy).

Distribution Layer: 3 × Cisco 2960 Switches (VLANs, Inter-VLAN Routing).

Access Layer: End devices, printers, and wireless access points for each floor.

🏢 Floor-wise Departments:
Floor	Departments
Ground Floor	Reception, Logistics, Store
First Floor	Sales, HR, Finance
Second Floor	IT, Administration
🌐 IP Addressing Scheme
Department	VLAN ID	Subnet	Host Range	Broadcast
IT	10	192.168.1.0/24	192.168.1.1–254	192.168.1.255
Administration	20	192.168.2.0/24	192.168.2.1–254	192.168.2.255
Sales	30	192.168.3.0/24	192.168.3.1–254	192.168.3.255
HR	40	192.168.4.0/24	192.168.4.1–254	192.168.4.255
Finance	50	192.168.5.0/24	192.168.5.1–254	192.168.5.255
Logistics	60	192.168.6.0/24	192.168.6.1–254	192.168.6.255
Store	70	192.168.7.0/24	192.168.7.1–254	192.168.7.255
Reception	80	192.168.8.0/24	192.168.8.1–254	192.168.8.255

Router Interlinks:

Floor 1 ↔ Floor 2 → 10.10.10.0/30

Floor 1 ↔ Floor 3 → 10.10.10.4/30

Floor 2 ↔ Floor 3 → 10.10.10.8/30

🛡️ Security Implementation

Access Control Lists (ACLs): Restrict cross-VLAN communication (Finance/Administration protected).

Port Security: Allows only trusted MAC addresses per switch port.

SSH Configuration: Secure remote access for network admins.

NAT/PAT: Provides secure external access through a single public IP.

⚙️ Key Configurations
VLAN and Port Setup

Each department VLAN is assigned a range of access ports, while trunk links carry multiple VLANs across switches.
Layer 3 Switch SVIs handle Inter-VLAN Routing internally for improved performance.

Routing

OSPF Dynamic Routing: Enables automatic route discovery between floors.

DHCP: Centralized IP allocation from IT Department server.

NAT/PAT: Configured for internet access sharing.

📊 Quality of Service (QoS)

QoS prioritization ensures:

🎤 Voice Traffic: 30% reserved bandwidth

🎥 Video Traffic: 20% reserved bandwidth

💻 Default Data Traffic: Remaining bandwidth shared equally

🧠 Monitoring & Management

Regular use of show commands: show ip route, show vlan, show access-lists

Configuration backups with copy running-config startup-config

Syslog & SNMP (recommended for real deployment)

Continuous fault monitoring through Cisco Packet Tracer simulation

✅ Testing & Validation

Simulation in Cisco Packet Tracer validated:

VLAN & Inter-VLAN communication

DHCP, OSPF, and NAT/PAT functionality

ACL-based security enforcement

Redundancy and performance (latency < 2 ms)

Successful troubleshooting and optimization

📈 Results
Metric	Result
Network Latency	< 2 ms
DHCP Response	< 1 sec
Packet Delivery	100%
OSPF Failover	Automatic redundancy
Unauthorized Access	Blocked successfully
🏁 Conclusion

The Hotel Management System Network was successfully designed and simulated with full functionality, secure segmentation, and redundancy. It provides a realistic and scalable enterprise-grade network suitable for hotel operations, serving as a solid foundation for IoT-based smart systems in the future.

👨‍💻 Team Members
Name	Register No.
Yash Agarwal	RA2311033010055
Aaniya Jain	RA2311033010057
Piyushi Singhal	RA2311033010066
Neha Kadaiyala	RA2311033010093
🏫 Institution

Department of Data Science and Business Systems
School of Computing, Faculty of Engineering and Technology
SRM Institute of Science and Technology, Kattankulathur

📚 Reference

[1] Cisco Networking Academy, Routing and Switching Essentials v6 Companion Guide, Cisco Press, 2016.
