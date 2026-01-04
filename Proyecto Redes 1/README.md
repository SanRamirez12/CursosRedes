# Networks I Project – Contabiliza S.A.  
**DHCP & DNS Server Configuration and Segmented Enterprise Network Infrastructure**

---

## General Description
This project aims at the **complete modernization of the network infrastructure** of the accounting company **Contabiliza S.A.**, through the **implementation of internal network services** and **logical segmentation using VLANs**.  
The design was developed as part of the course **Networks I (BIS-13)** at the **Universidad Latina de Costa Rica**, applying real-world networking engineering standards and methodologies.

The project covers the **configuration of DHCP and DNS servers**, the **integration of an internal mail server**, a **corporate intranet**, and the **implementation of structured cabling** based on **Category 6**, along with **Wi-Fi 6 wireless access points**, all validated through simulation in **Cisco Packet Tracer**.

---

## Project Objectives

- Automate IP address assignment using a **centralized DHCP server**.  
- Implement an **internal DNS server** for local name resolution.  
- Segment the network using **VLANs** for each department (Administration, Sales, Technical Support, Warehouse, and Services).  
- Integrate internal services: **email (SMTP/IMAP)** and a **corporate web intranet**.  
- Improve the **security, performance, and scalability** of the company’s network.  
- Comply with current **cabling standards and IEEE protocols**.

---

## General Network System Architecture

The design is based on an **enterprise hierarchical architecture**:

### Access Layer
- Managed switches with VLANs (Administration, Sales, Support, Warehouse, Services).  
- **Cat 6 structured cabling** according to the **TIA/EIA-568** standard.  
- Integration of **Wi-Fi 6 (802.11ax)** wireless access points.

### Distribution Layer
- Routers with **inter-VLAN routing** and optimized **VLSM subnetting**.  
- Configuration of access policies and internal addressing per department.

### Core / Server Layer
- **DHCP Server:** Dynamic IP assignment segmented by VLAN.  
- **DNS Server:** Internal name resolution (e.g., `intranet.contabiliza.local`).  
- **Web Server:** Corporate intranet for news, documents, and internal resources.  
- **Mail Server:** SMTP/IMAP under an internal domain (`@contabiliza.local`).

---

## Technologies and Tools

| Category | Technologies |
|---------|--------------|
| **Simulation** | Cisco Packet Tracer |
| **Network Protocols** | VLANs, DHCP, DNS, SMTP/IMAP, HTTP, ICMP |
| **Hardware (simulated)** | TP-Link BE19000 Routers, Managed Gigabit Switches, Wi-Fi 6 Access Points |
| **Cabling** | Category 6 (TIA-568), Patch Panels, RJ45 |
| **Operating Systems** | Windows Server 2022, Ubuntu Server |
| **Implemented Services** | DHCP, DNS, Mail Server, Web Server (Intranet) |
| **Applied Standards** | IEEE 802.3, IEEE 802.11ax, ISO/IEC 27001, TIA-568 |

---

## IP Addressing Plan

| Department | VLAN | Subnet | IP Range | Gateway |
|------------|------|--------|----------|----------|
| Administration | 10 | 192.168.10.0/26 | .1–.62 | 192.168.10.1 |
| Sales | 20 | 192.168.20.0/25 | .1–.126 | 192.168.20.1 |
| Technical Support | 30 | 192.168.30.0/27 | .1–.30 | 192.168.30.1 |
| Warehouse | 40 | 192.168.40.0/28 | .1–.14 | 192.168.40.1 |
| Services | 50 | 192.168.50.0/28 | .1–.14 | 192.168.50.1 |

---

## Security and Best Practices

- VLAN-based segmentation to isolate traffic between departments.  
- Secure passwords and role-based access (console, VTY).  
- Firewall policies and ACLs to control inter-VLAN access.  
- Protected and authenticated internal servers within the local network.  
- Structured cabling compliant with TIA/EIA-568 to minimize interference.  
- Traffic control and prioritization through QoS and centralized management.

---

## Validation Tests

✅ **DHCP:** Automatic IP assignment per VLAN.  
✅ **DNS:** Correct resolution of internal domains.  
✅ **Internal Mail:** Local sending and receiving via SMTP/IMAP.  
✅ **Intranet:** Internal web access from all departments.  
✅ **Wi-Fi:** Stable connectivity using WPA3 and VLAN assignment.  
✅ **Simulation:** Connectivity validated in Cisco Packet Tracer with no packet loss.

---

## Main Results

- Elimination of IP conflicts and a 100% reduction in manual configurations.  
- Improved network performance and internal traffic segregation.  
- Stable and secure wireless network with full coverage.  
- Successful integration of internal services (DNS, mail, intranet).  
- Scalability for future expansions without complete redesign.

---

## Future Recommendations

- Implement server redundancy (DHCP/DNS clusters).  
- Add **real-time monitoring (SNMP/Nagios)**.  
- Apply advanced security policies (IDS/IPS, additional segmentation).  
- Migrate critical services to a hybrid infrastructure (on-premise + cloud).  
- Document preventive maintenance and expansion plans.

---

## Authors

- **Santiago Ramírez Elizondo**  
- **Jonatan Fabricio Grande López**

Instructor: *Bryan Vega Rondón*  
Course: *Networks I – Universidad Latina de Costa Rica*  
Date: *April 2025*

---

## Included Files

-  `ProyectoContabilizaSA_Redes1.pkt` → Cisco Packet Tracer topology  
-  `Technical_Documentation.pdf` → Configuration details, VLANs, DHCP/DNS  
-  `README.md` → This document

---

##  License
Academic project for educational purposes.  
You may use this content as a reference by citing the authors and the institution.

---
