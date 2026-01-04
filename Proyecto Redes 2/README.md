# Final Project – Networks II  
**Design and Implementation of a Segmented Network Infrastructure with VLANs, Integrated Services, and Basic Cybersecurity**

---

## General Description
This project presents the design and implementation of a **segmented network infrastructure** for the fictional company **NexaCapital S.A.**, dedicated to financial and investment services.  
The main objective was to build a **scalable, secure, and functional** network within a multi-department environment, integrating essential services such as **DNS, DHCP, corporate email, HTTP intranet**, and basic **cybersecurity mechanisms** through **ACLs** and **VLAN-based segmentation**.

---

## Main Objectives

- **Design a hierarchical network** following the layered model (Access – Distribution – Core).  
- **Segment the network** using VLANs to improve security and performance.  
- **Automate network services** with DNS, DHCP, and internal email.  
- **Implement dynamic routing protocols** (OSPF and BGP) to ensure internal and external connectivity.  
- **Apply basic security measures**, such as ACLs, secure passwords, and port protection.  
- **Comply with international standards** such as ISO 27001 and Costa Rica’s Personal Data Protection Law (Law 8968).

---

## General Architecture

**Hierarchical network topology:**
- **Access layer:** Managed switches with VLANs 10 (Finance), 20 (HR), 30 (Administration), and 40 (IT).  
- **Distribution layer:** Intermediate routers using *router-on-a-stick* configuration and OSPF.  
- **Core layer:** Main router connected to the ISP with an established BGP session for route exchange.

**Integrated services:**
- **DNS:** Internal name resolution (Bind / Windows Server).  
- **DHCP:** Dynamic IP address assignment per VLAN.  
- **HTTP:** Corporate intranet accessible from all departments.  
- **Corporate email:** SMTP / POP3 configured for internal communication.  
- **ACLs:** Traffic control between departments for logical segmentation and security.

---

## Technologies Used

| Category | Technologies |
|----------|--------------|
| **Simulation** | Cisco Packet Tracer |
| **Protocols** | VLANs, OSPF, BGP, DHCP, DNS, SMTP/POP3, HTTP |
| **Security** | ACLs, Port-Security, Password Encryption, BPDU Guard |
| **Applied Standards** | IEEE 802.1Q, 802.11ax, ISO/IEC 27001, TIA-568, Law 8968 |
| **Simulated Hardware** | Routers, switches, servers, PCs, access points |

---

## IP Addressing Plan

| Department | VLAN | Subnet | IP Range | Gateway |
|------------|------|--------|----------|----------|
| Finance | 10 | 192.168.0.0/25 | .0 – .127 | 192.168.0.1 |
| HR | 20 | 192.168.0.128/26 | .128 – .191 | 192.168.0.129 |
| Administration | 30 | 192.168.0.192/26 | .192 – .255 | 192.168.0.193 |
| IT | 40 | 192.168.1.0/27 | .0 – .31 | 192.168.1.1 |

/30 serial links between routers and ISP connection using BGP (network 10.0.0.0/30).

---

## Security Measures

- **ACL configuration** to limit inter-VLAN traffic.  
- **Encrypted passwords** and authentication on console and VTY lines.  
- **Port-Security** and **BPDU Guard** on access switches.  
- Secure password policies and **access control** enforcement.  
- Segmentation and isolation of sensitive traffic by department.

---

## Tests Performed

- **Internal connectivity:** Successful ping between VLANs via OSPF.  
- **DHCP/DNS:** Automatic IP assignment and correct resolution of internal domains.  
- **HTTP:** Functional corporate intranet from all departments.  
- **Email:** SMTP functional; POP3 partially successful (server tuning pending).  
- **BGP:** Session established with ISP (pending NAT redistribution for external ping).  
- **Security:** No port-security violations; ACLs planned and tested.

---

## Results and Lessons Learned

- **Full connectivity achieved** between departments with correct DNS/DHCP service operation.  
- **BGP session established** with the ISP and OSPF running between internal routers.  
- **Successful VLAN segmentation** and controlled inter-department traffic.  
- Identified improvement areas: BGP→OSPF redistribution and POP3 configuration.  
- Applied best practices in documentation, naming conventions, and standardization.

---

## Technical Recommendations

- Implement **SSH**, **AAA**, and **OSPF authentication** to strengthen security.  
- Add **HSRP/VRRP** and **EtherChannel** for high availability.  
- Include **DHCP Snooping**, **DAI**, and **QoS** for voice/data traffic.  
- Document configurations and maintain automated backups.  
- Prepare gradual migration to a **hybrid infrastructure (on-premise + cloud)**.

---

## Authors

- **Santiago Ramírez Elizondo**  
- **David Abarca Chaves**  
- **Alberto Álvarez Navarro**  
- **Sebastián Chaves Solano**

Instructor: *Daniel Adolfo Ramírez González*  
Course: *BTI-13 Networks II – Universidad Latina de Costa Rica*  
Date: *August 2025*

---

## 🏁 License
This project was developed for educational purposes under the **Networks II** course.  
You may use it as an academic reference by citing the authors.

---
