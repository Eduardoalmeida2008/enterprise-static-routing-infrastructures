# Enterprise LAN: Segmentation & Link Aggregation
### VLANs, EtherChannel, and Inter-VLAN Routing (Project 2.2)

**Author:** Eduardo Mello De Almeida  
**Date:** January 2026  
**Status:** Completed & Connectivity Verified

---

## 📌 Project Overview
Small Business Network design using Cisco Packet Tracer. Features a single-switch architecture with VLAN segmentation and Inter-VLAN routing (Router-on-a-Stick). Implements static IP planning and EtherChannel for optimized link performance.

---

## 🛠️ Technical Implementation (Verified Evidence)
* **Inter-VLAN Routing:** **Router-on-a-Stick** architecture using sub-interfaces for cross-VLAN communication.
* **Layer 2 Segmentation:** Specific **VLANs** created to isolate departmental broadcast domains.
* **Trunking:** **802.1Q** encapsulation active on all uplinks between the router and switches.
* **Static Addressing:** Network-wide IP planning verified through end-to-end connectivity tests.

---

## 🖼️ Technical Documentation

### 1. Network Topology
The physical and logical layout of the network, showing the interconnection between hosts, switches, and the gateway.

![Logical Topology](01_Full_Network_Topology.png)

---

### 2. High-Speed Backbone (EtherChannel)
Verification of the link aggregation. Multiple physical interfaces were combined into a single logical Port-Channel for increased reliability.

| Port-Channel Summary | Trunking Status |
|---|---|
| ![EtherChannel Status](04_Vlan_Brief_SW.png) | ![Trunk Status](02_Switch_VLAN_Database.png) |
*Figure: Evidence of operational EtherChannel and active Trunk links.*

---

### 3. Layer 3 Routing (Inter-VLAN)
Detailed view of the router's configuration, showing the sub-interfaces responsible for routing traffic between the segmented VLANs.

![Router Config](03_Router_Subinterfaces.png)
*Figure: Router-on-a-Stick sub-interface configuration.*

---

### 4. Connectivity Validation (End-to-End)
Successful ICMP "Ping" tests proving that the static routing and VLAN tagging are correctly configured throughout the topology.

![Connectivity Test](08_Test_connectivity_Ping_Others_Gateways.png) 
*Figure: Final connectivity verification between different network segments.*

---

## 📂 Repository Structure
* `📂 configs/` - Cisco Packet Tracer source file (.pkt).
* `📂 screenshots/` - Step-by-step technical evidence (01-15).
* `📄 README.md` - Technical documentation.

---

## 🚀 How to Run
1. Open the `.pkt` file in **Cisco Packet Tracer**.
2. Verify the **EtherChannel** status by checking the consolidated links between switches.
3. Test connectivity by performing a ping between any two PCs in different VLANs to observe the **Router-on-a-Stick** functionality in action.

---
**Focus: Static Network Engineering & Layer 2 Performance.**
