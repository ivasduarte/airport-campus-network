# RCOMP 2025-2026: Project 1 Sprint 2 Member 1241229 File

### Contents

1. [Network Base Data](#1-network-base-data)
2. [Subnetting (VLSM)](#2-subnetting-vlsm)
    - [Wi-Fi VLAN](#21-wi-fi-vlan-t4vlan808)
    - [VLAN User Outlets](#22-vlan-user-outlets-t4vlan807)
    - [VLAN VoIP](#23-vlan-voip-t4vlan809)
    - [DMZ VLAN Servers](#24-dmz-vlan-servers-t4vlan810)
3. [IP Address Assignment](#3-ip-address-assignment-end-devices-and-interfaces)
4. [Static Routing Table](#4-static-routing-table)

---

## 1. Network Base Data

According to the team planning meeting, the following parameters were defined for Terminal 4:
* **IPv4 Block Assigned to Terminal 4:** 10.75.192.0/20
* **VLAN IDs Assigned:** 807 to 810
* **Campus Backbone Network:** 10.75.208.0/24
* **Router IP on Backbone:** 10.75.208.4
* **DMZ Switch Network:** 10.75.210.0/23
---
## 2. Subnetting (VLSM)

To accommodate the node requirements of Terminal 4, the block `10.75.192.0/20` was subdivided from the largest network to the smallest:

### 2.1. Wi-Fi VLAN (T4VLAN808)
* **Requirement:** 1800 nodes
* **Required Size:** 2046 usable IPs → /21 mask (255.255.248.0)
* **Network Address:** 10.75.192.0/21
* **First Usable IP (Gateway):** 10.75.192.1
* **Last Usable IP:** 10.75.199.254
* **Broadcast Address:** 10.75.199.255

### 2.2. VLAN User Outlets (T4VLAN807)
* **Requirement:** 800 nodes
* **Required Size:** 1022 usable IPs → /22 mask (255.255.252.0)
* **Network Address:** 10.75.200.0/22
* **First Usable IP (Gateway):** 10.75.200.1
* **Last Usable IP:** 10.75.203.254
* **Broadcast Address:** 10.75.203.255

### 2.3. VLAN VoIP (T4VLAN809)
* **Requirement:** 400 nodes
* **Required Size:** 510 usable IPs → /23 mask (255.255.254.0)
* **Network Address:** 10.75.204.0/23
* **First Usable IP (Gateway):** 10.75.204.1
* **Last Usable IP:** 10.75.205.254
* **Broadcast Address:** 10.75.205.255

### 2.4. DMZ VLAN Servers (T4VLAN810)
* **Requirement:** 120 nodes
* **Required Size:** 126 usable IPs → /25 mask (255.255.255.128)
* **Network Address:** 10.75.206.0/25
* **First Usable IP (Gateway):** 10.75.206.1
* **Last Usable IP:** 10.75.206.126
* **Broadcast Address:** 10.75.206.127

---

## 3. IP Address Assignment (End Devices and Interfaces)

To ensure that the networks are functional in the Packet Tracer simulation, the following IPs were statically configured
on the test devices:

|    Device    |     VLAN      |      IP      |      Mask       |     Gateway      |
|:------------:|:-------------:|:------------:|:---------------:|:----------------:|
|   T4-PC-L0   |  807 (User)   | 10.75.200.2  |  255.255.252.0  |   10.75.200.1    |
|   T4-PC-L2   |  807 (User)   | 10.75.200.3  |  255.255.252.0  |   10.75.200.1    |
| T4-Laptop-L0 |  808 (Wi-Fi)  | 10.75.192.2  |  255.255.248.0  |   10.75.192.1    |
| T4-Laptop-L2 |  808 (Wi-Fi)  | 10.75.192.3  |  255.255.248.0  |   10.75.192.1    |
|  T4-VoIP-L0  |  809 (VoIP)   |      -       |        -        |        —         |
|  T4-VoIP-L2  |  809 (VoIP)   |      -       |        -        |        —         |
| T4-Server-L0 | 810 (Servers) | 10.75.206.2  | 255.255.255.128 |   10.75.206.1    |
| T4-Server-L2 | 810 (Servers) | 10.75.206.3  | 255.255.255.128 |   10.75.206.1    |
| T4-PC-DMZ-L0 |  798 (SwDMZ)  | 10.75.210.15 |  255.255.254.0  | Isolated Network |
| T4-PC-DMZ-L2 |  798 (SwDMZ)  | 10.75.210.30 |  255.255.254.0  | Isolated Network |

### Router T4 Subinterfaces

| Subinterface | VLAN |     IP      |      Mask       |
|:------------:|:----:|:-----------:|:---------------:|
|  Fa0/0.797   | 797  | 10.75.208.4 |  255.255.255.0  |
|  Fa0/0.807   | 807  | 10.75.200.1 |  255.255.252.0  |
|  Fa0/0.808   | 808  | 10.75.192.1 |  255.255.248.0  |
|  Fa0/0.809   | 809  | 10.75.204.1 |  255.255.254.0  |
|  Fa0/0.810   | 810  | 10.75.206.1 | 255.255.255.128 |

### Switch Management IPs (Switches DMZ – VLAN 798)

|  Switch  |      IP      |     Mask      |
|:--------:|:------------:|:-------------:|
|  T4-MC   | 10.75.210.10 | 255.255.254.0 |
| T4-IC-L0 | 10.75.210.11 | 255.255.254.0 |
| T4-IC-L2 | 10.75.210.12 | 255.255.254.0 |
| T4-HC-L0 | 10.75.210.13 | 255.255.254.0 |
| T4-HC-L2 | 10.75.210.14 | 255.255.254.0 |

---

## 4. Static Routing Table

Terminal 4's router (model 2811) is connected to the Campus Backbone via IP `10.75.208.4`

To reach the networks of the other terminals and the Internet, the following static routes were configured:

| Destination Network (IP Block) |     Mask      | Next-Hop (IP of the Destination Router on the Backbone) |             Description              |
|:------------------------------:|:-------------:|:-------------------------------------------------------:|:------------------------------------:|
|          10.75.160.0           | 255.255.240.0 |                       10.75.208.2                       |         Route to Terminal 2          |
|          10.75.176.0           | 255.255.240.0 |                       10.75.208.3                       |         Route to Terminal 3          |
|          10.75.128.0           | 255.255.224.0 |                       10.75.208.5                       |         Route to Terminal 5          |
|            0.0.0.0             |    0.0.0.0    |                       10.75.208.2                       | Standard Route for Internet (via T2) |
 