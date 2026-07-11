# FIFA-Fan-Park-Final-Project
Final Project - CSCE 3530.401 - Dr. Ali Zarafshani - Yan Qiao

This network is mainly built around a 1 router system (R1). This router connects to 3 separate “zones”: Fan zone, Staff zone, Server zone. Each zone includes it’s own switch and end-device(s). Using a zone logic we can make separate subnets, keep traffic limited, involve NAT, etc. Using 1 router allows us to configure DHCP pools and that allows the zones to be scalable. The “PC-Fan” & “PC-Staff” are both using DHCP for their addressing. The “Serv1” server is a static server that runs DNS and HTTP/HTTPS services for the network. One router, Three switches, Three subnets. This is a simple topology that can be scaled indefinitely. 

#IP ADDRESS TABLE


| Device | Interface / Transport | IP Address | Description |
| :--- | :--- | :--- | :--- |
| **R1** | Gig0/0 | `192.168.1.1 /24` | Fan Zone |
| **R1** | Gig0/1 | `192.168.2.1 /24` | Staff Zone |
| **R1** | Gig0/2 | `192.168.3.1 /24` | Server Zone |
| **PC-Fan** | FastEthernet0 | `192.168.1.2 /24` | Fan Zone PC (DHCP) |
| **PC-Staff** | FastEthernet0 | `192.168.2.2 /24` | Staff Zone PC (DHCP) |
| **Serv1** | Network | `192.168.3.10 /24` | DNS Server & HTTP/HTTPS Server (static) |
