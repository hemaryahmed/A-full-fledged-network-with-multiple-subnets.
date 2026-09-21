This project designs and simulates a complete network infrastructure for a fictional institution, University of Scholars, connecting 5 campuses through 6 routers, supporting wired and wireless devices, and centrally managing core services (Web, DNS, DHCP).

Features
1. 5 interconnected campuses with independent LANs
2.  Wired and wireless connectivity (Access Points for laptops/smartphones)
3.  Centralized Web, DNS, and DHCP server
4.  Dynamic routing with OSPF across all campus routers
5. Subnetting using Class A addressing (10.0.0.0, 11.0.0.0, 12.0.0.0, 13.0.0.0, 15.0.0.0)
6. Inter-router links on separate subnets (60.0.0.0, 70.20.0.0, 80.30.0.0, 90.40.0.0, 100.50.0.0)
7. DHCP relay via ip helper-address for remote-network IP assignment
8. Verified end-to-end connectivity via ping tests across campuses
9. Tools Used
    
Tool	Purpose:
1. Cisco Packet Tracer (v6.2.0.0052)	Network simulation
2. 2960 Switches	LAN switching
3. Generic Routers	Inter-campus routing
4. Access Point-PT	Wireless connectivity
5. Server-PT	Combined Web / DHCP / DNS server

Network Architecture:
5 campuses, each with its own switch, PCs, laptops, and wireless AP
Routers interconnected in a mesh-like topology for redundancy

Central server segment hosting:
- Web Server → 10.0.0.150
- DNS Server → 10.0.0.100
- DHCP Server → 10.0.0.200


Configuration Highlights:
1. OSPF Area 0 configured on all 5 routers for dynamic route sharing
2. Serial links between routers with clock rate 64000
3. DHCP scopes created per subnet with correct default gateways
4. DNS A Record mapping www.scholars.edu.bd → 10.0.0.150

Limitations
1. Wireless devices occasionally auto-connect to the nearest AP instead of the intended one
2. Initial DHCP & routing misconfigurations required troubleshooting via ip helper-address

Future Scalability:

The network can grow easily thanks to OSPF and subnetting:
Add more switches, APs, and hosts to existing LANs
Connect new campuses by adding routers and links
No need to redesign existing configuration

Testing:
Successful ping test between PC5 (12.0.0.3) and Laptop 6 (13.0.0.3) confirmed full connectivity across different subnets.

- Author
Hemary Ahmed
