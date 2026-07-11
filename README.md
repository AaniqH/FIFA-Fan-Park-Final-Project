# FIFA-Fan-Park-Final-Project
Final Project - CSCE 3530.401 - Dr. Ali Zarafshani - Yan Qiao

This network is mainly built around a 1 router system (R1). This router connects to 3 separate “zones”: Fan zone, Staff zone, Server zone. Each zone includes it’s own switch and end-device(s). Using a zone logic we can make separate subnets, keep traffic limited, involve NAT, etc. Using 1 router allows us to configure DHCP pools and that allows the zones to be scalable. The “PC-Fan” & “PC-Staff” are both using DHCP for their addressing. The “Serv1” server is a static server that runs DNS and HTTP/HTTPS services for the network. One router, Three switches, Three subnets. This is a simple topology that can be scaled indefinitely. 

# IP ADDRESS TABLE


| Device | Interface / Transport | IP Address | Description |
| :--- | :--- | :--- | :--- |
| **R1** | Gig0/0 | `192.168.1.1 /24` | Fan Zone |
| **R1** | Gig0/1 | `192.168.2.1 /24` | Staff Zone |
| **R1** | Gig0/2 | `192.168.3.1 /24` | Server Zone |
| **PC-Fan** | FastEthernet0 | `192.168.1.2 /24` | Fan Zone PC (DHCP) |
| **PC-Staff** | FastEthernet0 | `192.168.2.2 /24` | Staff Zone PC (DHCP) |
| **Serv1** | Network | `192.168.3.10 /24` | DNS Server & HTTP/HTTPS Server (static) |


# CHALLENGES FACED AND SOLUTIONS 
I faced a good 2 challenges whilst working on this project. This is my second time ever using packettracer so I used a good amount of forums and youtube videos as my aid. One challenge I faced was that I kept making typos and since packettracer is an old tool and how the font is old I got my numbers mixed up several times. I typed an incorrect subnet of 169 instead of 168 and that made it so the FAN-Zone never worked. Another instance where I made a type and it took me a long time to find was when I configured the DHCP pool for the fan zone with the wrong network which didn’t get my pc in the fan zone an address. I reconfigured it and everything started going back into the right place. All the challenges I faced were mostly human errors, one that really took me the longest time was that my DNS never worked. I tried everything to get it to work and realized that my theme (dark mode) made the on and off disappear so it wasn’t even on. Once I turned it on it was alright. Solutions are to make sure you understand everything and have a checklist near your ip table and check it off after double checking whether it was assigned or not. I also recommend just using the classic theme on packettracer. 

# Legacy beats everything. 

# CONCLUSION

This network demonstrates all the protocols for this final project. I also tested it to make sure everything worked properly. I checked and pinged the devices and I followed my notes as I assigned the end devices. This was a great project and starting from scratch and building a computer network was edifying. 

