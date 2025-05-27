# Computer Networks Simulation Project – CS-3001

## Project Overview

This project demonstrates a full-scale enterprise network simulation designed and implemented using Cisco Packet Tracer. The simulation includes 21 routers, multiple LANs (Networks A–N), dynamic routing protocols, VLSM subnetting, NAT, ACLs, and server configuration for DNS, DHCP, FTP, Mail, and HTTP.

The goal is to design and configure an end-to-end functional network as per the specifications provided in the project guidelines, with proper routing, address allocation, and service control.

---

## Tools Used

- Cisco Packet Tracer (Instructor Version)
- VLSM Calculator (online)
- Manual subnetting and planning
- Google Sheets (for IP allocations)
- GitHub (for version control and documentation)

---

## Key Features & Configuration Summary

### 1. Network Design
- Total 14 logical networks: A to N
- Devices include routers, switches, PCs, laptops, smartphones, and servers
- Wired and wireless connectivity simulated

### 2. IP Addressing (VLSM)
- VLSM applied based on required host counts per network
- Separate /30 subnets created for 30 point-to-point router links
- Address range: 192.168.0.0/16 and beyond, including public IP 203.0.113.31 for NAT

### 3. Routing Protocols
- OSPF (Areas 0, 1, 2), EIGRP, and RIP configured as per network block labels
- Proper redistribution implemented on routers connecting different protocol zones

### 4. NAT (Network Address Translation)
- Configured on:
  - Router10 (for Network F)
  - Router21 (for Network K)
- NAT uses the assigned public IP: 203.0.113.31

### 5. DHCP Configuration
- Centralized DHCP Server placed in Block D
- Hosts in all EIGRP, OSPF Area 1 & 2, and RIP networks receive dynamic IPs via DHCP relay

### 6. ACLs (Access Control Lists)
- Restrictions enforced to deny web access from:
  - One PC in Network A
  - One laptop in Network E
  - One smartphone in Network B
  - All hosts in Network D
- ACLs applied on the router connected to the Web Server

### 7. Servers & Services
- Mail Server (in Block D): Only hosts in Network H and I can send and receive email
- FTP Server: Only hosts in Network G can access and upload files
- Web Server: Accessible to all except blocked devices via ACLs
- DNS configured to resolve domain names for clients

---

## File Contents

- `CS-3001-CNET-Project.pkt`: Cisco Packet Tracer simulation file
- `README.md`: Project documentation and summary
- `subnetting_plan.xlsx`: VLSM and IP assignment breakdown (optional)
- `screenshots/`: Key screenshots of configurations and ping tests (optional)

---

## How to Run

1. Open the `.pkt` file using Cisco Packet Tracer (Instructor version recommended)
2. Verify router configurations by checking each routing protocol
3. Test connectivity using `ping`, `tracert`, and browser-based services from end devices
4. Use simulation mode to observe packet flow between services (e.g., HTTP, FTP, DNS)

---

## Author

**Muhammad Akash Waris**  
Roll No: 23I-2110  
Department of Computer Science  
Course: CS-3001 – Computer Networks

---

## Note

This project was developed under academic guidelines. All configurations were created from scratch following proper subnetting, routing, and service design principles. No external configuration files or cheating was involved in the setup.

