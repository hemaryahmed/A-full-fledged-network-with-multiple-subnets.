🌐 University of Scholars — Multi-Campus Network Design

A full-fledged campus network design project built for CSE405 (Computer Networks), East West University — simulating a 5-campus university network with dynamic routing, centralized services, and both wired & wireless connectivity.

📖 Overview

This project designs and simulates a complete network infrastructure for a fictional institution, University of Scholars, connecting 5 campuses through 6 routers, supporting wired and wireless devices, and centrally managing core services (Web, DNS, DHCP).

✨ Features
🏫 5 interconnected campuses with independent LANs
📡 Wired and wireless connectivity (Access Points for laptops/smartphones)
🌍 Centralized Web, DNS, and DHCP server
🔁 Dynamic routing with OSPF across all campus routers
🧩 Subnetting using Class A addressing (10.0.0.0, 11.0.0.0, 12.0.0.0, 13.0.0.0, 15.0.0.0)
🔗 Inter-router links on separate subnets (60.0.0.0, 70.20.0.0, 80.30.0.0, 90.40.0.0, 100.50.0.0)
📥 DHCP relay via ip helper-address for remote-network IP assignment
✅ Verified end-to-end connectivity via ping tests across campuses
🛠️ Tools Used
Tool	Purpose
Cisco Packet Tracer (v6.2.0.0052)	Network simulation
2960 Switches	LAN switching
Generic Routers	Inter-campus routing
Access Point-PT	Wireless connectivity
Server-PT	Combined Web / DHCP / DNS server
🗺️ Network Architecture
5 campuses, each with its own switch, PCs, laptops, and wireless AP
Routers interconnected in a mesh-like topology for redundancy
Central server segment hosting:
🌐 Web Server → 10.0.0.150
🧭 DNS Server → 10.0.0.100
📦 DHCP Server → 10.0.0.200
⚙️ Configuration Highlights
OSPF Area 0 configured on all 5 routers for dynamic route sharing
Serial links between routers with clock rate 64000
DHCP scopes created per subnet with correct default gateways
DNS A Record mapping www.scholars.edu.bd → 10.0.0.150
🚧 Limitations
Wireless devices occasionally auto-connect to the nearest AP instead of the intended one
Initial DHCP & routing misconfigurations required troubleshooting via ip helper-address
📈 Future Scalability

The network can grow easily thanks to OSPF and subnetting:

Add more switches, APs, and hosts to existing LANs
Connect new campuses by adding routers and links
No need to redesign existing configuration
✅ Testing

Successful ping test between PC5 (12.0.0.3) and Laptop 6 (13.0.0.3) confirmed full connectivity across different subnets.

👤 Author

Hemary Ahmed ID: 2022-3-60-008 East West University — Dept. of CSE
