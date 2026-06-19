# 🏦 Secure Banking Network Infrastructure — Cisco Packet Tracer

> CCNA Final Project | Designed by **Ramy Osama** | Supervised by **Shaymaa Taref Sarhan**

A fully configured enterprise banking network simulation built in Cisco Packet Tracer. The design implements a multi-tier architecture with complete VLAN segmentation, inter-VLAN routing, EtherChannel LACP, and internal banking services (Web, Mail, DNS) under the private domain `cis.com`.

---

## 📋 Project Overview

This project simulates a real-world banking network environment using Cisco Packet Tracer. It focuses on security, isolation, and manageability — keeping departments separated, traffic controlled, and services centrally hosted.

---

## 🏗️ Network Architecture

```
           [ Router 2911 ]
                  |
       [ Core Multilayer Switch ]
                  |
    ┌─────────────┼─────────────┐
    │             │             │
[SW-Tellers] [SW-Mgmt/IT]  [SW-Servers]
  (VLAN 10)  (VLAN 20/30)   (VLAN 40)
    │             │             │
  PCs/         PCs/          Servers/
 Laptops      Printers       Printers
```

---

## 🔧 Features & Configuration

| Feature | Details |
|---|---|
| **VLAN Segmentation** | 4 VLANs for full department isolation |
| **Inter-VLAN Routing** | Router sub-interfaces (Router-on-a-Stick) |
| **802.1Q Trunking** | Tagged VLANs across uplink interfaces |
| **EtherChannel LACP** | Resilient, bundled uplinks |
| **DHCP** | Dynamic IP assignment per VLAN |
| **DNS** | Internal name resolution via `cis.com` |
| **Web Server** | Portal active at `www.cis-college.com` |
| **Mail Server** | SMTP & POP3 on internal domain `cis.com` |
| **Password Hardening** | Console & VTY access secured |
| **MOTD Banner** | Unauthorized access warning on all devices |

---

## 📡 VLAN & IP Addressing Scheme

| VLAN | Name | Subnet | Department |
|------|------|--------|------------|
| **10** | Tellers | `192.168.10.0/24` | Bank Teller workstations |
| **20** | Management | `192.168.20.0/24` | Management department |
| **30** | IT Support | `192.168.30.0/24` | IT Support team |
| **40** | Server Farm | `192.168.40.0/24` | Dedicated servers |

> **Server Farm DNS IP:** `192.168.40.10`

---

## 🖥️ Hardware Used (Simulated)

| Device | Model | Qty | Role |
|--------|-------|-----|------|
| Router | Cisco 2911 | 1 | Gateway & sub-interface routing |
| Core Switch | Multilayer | 1 | Backbone & inter-VLAN routing |
| Access Switches | Cisco 2960 | 3 | Departmental endpoint access |
| PCs | — | 10 | Daily user workstations |
| Laptops | — | 3 | Mobile user access |
| Printers | — | 3 | Networked printing |
| Servers | — | 4 | Web, Mail, DNS, DHCP |

---

## 🌐 Banking Services

| Service | Details |
|---------|---------|
| **Web Portal** | `www.cis-college.com` hosted on Server Farm |
| **Mail Server** | Internal `cis.com` domain — SMTP & POP3 |
| **DNS** | Resolves internal names to `192.168.40.10` |

---


## 🚀 Getting Started

### Prerequisites
- [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer) v8.x or higher

### How to Open
1. Clone or download this repository
2. Open **Cisco Packet Tracer**
3. Go to **File → Open** and select `project.pkt`
4. Explore the topology, VLANs, and device configurations

---

## 📚 Concepts Covered

- Multi-tier network architecture for enterprise environments
- VLAN design and broadcast domain segmentation
- Router-on-a-Stick for inter-VLAN routing
- 802.1Q trunking between switches and router
- EtherChannel with LACP for link aggregation
- DHCP server configuration per VLAN
- DNS and internal domain name resolution
- Web and mail server setup in a simulated LAN
- Network device hardening (passwords, banners)

---

## 👤 Author

**Ramy Osama**

---



---

> 💡 *"VLANs provide complete segmentation between departments — keeping services organized, traffic controlled, and the network easier to manage."*
