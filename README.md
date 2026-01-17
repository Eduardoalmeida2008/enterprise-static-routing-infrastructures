# Enterprise Static Routing Infrastructure

## 📖 Project Overview
This project demonstrates the manual implementation of a segmented enterprise network using **Cisco Packet Tracer**. The core focus is on **Static Routing**, providing total control over the traffic path and ensuring reliable communication between different network branches without the overhead of dynamic protocols.

## 🚀 Technical Implementation
* **Static Routing:** Manual configuration of `ip route` commands to establish deterministic paths across the network backbone.
* **Interface Management:** Systematic configuration of Gigabit and Serial interfaces with dedicated IPv4 addressing.
* **Network Segmentation:** Physical and logical separation of departments to optimize traffic and local management.
* **Connectivity Validation:** Comprehensive testing of the routing table and end-to-end data delivery.

## 🛠️ Technology Stack
* **Vendor:** Cisco Systems.
* **Protocols:** Static IPv4 Routing, ICMP.
* **Tool:** Cisco Packet Tracer 8.x.
* **Hardware:** Cisco ISR Routers, Catalyst Switches.

## 📊 Deployment Details
### 1. Layer 3 Configuration
Every interface was manually addressed. The status was verified using `show ip interface brief` to ensure all links were physically and logically active (Up/Up).

### 2. Static Routing Logic
To allow communication between non-adjacent networks, specific static routes were defined. This method ensures that the routing table is stable and predictable.

### 3. Connectivity Verification
The infrastructure was validated through:
- **Routing Table Analysis:** Using `show ip route` to confirm that all static paths are correctly installed.
- **End-to-End Pings:** Testing connectivity from the access layer of one segment to the remote gateway of another.
- **Simulation Flow:** Real-time analysis of packet forwarding through the routers.

---
**Developed by:** [Eduardo]
**Field:** Network Infrastructure & Implementation
