RCOMP 2025-2026: Project 1 Sprint 2 Member 1221176 File
=====

### Contents

1. [Network Base Data](#1-network-base-data)
2. [Subnetting (VLSM)](#2-subnetting-vlsm)
    - [Wi-Fi VLAN](#21-wi-fi-vlan-t5vlan803)
    - [VLAN User Outlets](#22-vlan-user-outlets-t5vlan804)
    - [VLAN VoIP](#23-vlan-voip-t5vlan805)
    - [DMZ VLAN Servers](#24-dmz-vlan-servers-t5vlan806)
3. [IP Address Assignment](#3-ip-address-assignment-end-devices-and-interfaces)
4. [Static Routing Table](#4-static-routing-table)

---

## 1. Network Base Data

According to the team planning meeting, the following parameters were defined for Terminal 5:
* **IPv4 Block Assigned to Terminal 5:** 10.75.128.0/19
* **VLAN IDs Assigned:** 803 to 806
* **Campus Backbone Network:** 10.75.208.0/24
* **DMZ Switch Network:** 10.75.210.0/23

---

## 2. Subnetting (VLSM)

To accommodate the node requirements of Terminal 5, the block ´10.75.128.0/19` was subdivided from the largest network to the smallest:

### 2.1. Wi-Fi VLAN (T5VLAN803)
* **Requirement:** 4000 nodes
* **Required Size:** 4094 usable IPs → /20 mask
* **Network Address:** 10.75.128.0/20
* **First Usable IP (Gateway):** 10.75.128.1
* **Last Usable IP:** 10.75.143.254
* **Broadcast Address:** 10.75.143.255
* **Subnet Mask:** 255.255.240.0


### 2.2. VLAN User Outlets (T5VLAN804)
* **Requirement:** 1900 nodes
* **Required Size:** 2046 usable IPs → /21 mask
* **Network Address:** 10.75.144.0/21
* **First Usable IP (Gateway):** 10.75.144.1
* **Last Usable IP:** 10.75.151.254
* **Broadcast Address:** 10.75.151.255
* **Subnet Mask:** 255.255.248.0


### 2.3. VLAN VoIP (T5VLAN806)
* **Requirement:** 500 nodes
* **Required Size:** 510 usable IPs → /23 mask
* **Network Address:** 10.75.152.0/23
* **First Usable IP (Gateway):** 10.75.152.1
* **Last Usable IP:** 10.75.153.254
* **Broadcast Address:** 10.75.153.255
* **Subnet Mask:** 255.255.254.0


### 2.4. DMZ VLAN Servers (T5VLAN805)
* **Requirement:** 200 nodes
* **Required Size:** 254 usable IPs → /24 mask
* **Network Address:** 10.75.154.0/24
* **First Usable IP (Gateway):** 10.75.154.1
* **Last Usable IP:** 10.75.154.254
* **Broadcast Address:** 10.75.154.255
* **Subnet Mask:** 255.255.255.0

---

## 3. IP Address Assignment (End Devices and Interfaces)

To ensure that the networks are functional in the Packet Tracer simulation, the following IPs were statically configured 
on the test devices:

|     **Device**      | **VLAN** |         **Device IP**          | **Subnet Mask** | **Default Gateway** |
|:-------------------:|:--------:|:------------------------------:|:---------------:|:-------------------:|
|  **Access Point**   |   803    |          10.75.128.10          |  255.255.240.0  |     10.75.128.1     |
|  **PC (Outlets)**   |   804    |          10.75.144.10          |  255.255.248.0  |     10.75.144.1     |
|     **Server**      |   805    |          10.75.154.10          |  255.255.255.0  |     10.75.154.1     |
| **IP Phone (VoIP)** |   806    | Configure via DHCP in Sprint 3 |        -        |          -          |

---

## 4. Switches Configuration (VLAN 798)

A switch management zone (DMZ) is a dedicated and isolated network, without a router/gateway. 

- **Switch Configuration:** The VLAN 798 must be created on each switch and assigned an IP address.

### 4.1. Sub-Interfaces

The router (model 2811) will be the "Default Gateway" for VLANs 803, 804, 805, and 806. The connection from the router
to the main switch (main cross-connect) must be made on a port in *Trunk Mode*. 

```
// for Wi-Fi VLAN
interface FastEthernet0/0.803
encapsulation dot1Q 803
ip address 10.75.128.1 255.255.240.0

// for pcs/users VLAN
interface FastEthernet0/0.804
encapsulation dot1Q 804
ip address 10.75.144.1 255.255.248.0

// for servers VLAN
interface FastEthernet0/0.805
encapsulation dot1Q 805
ip address 10.75.154.1 255.255.255.0

// for VoIP VLAN
interface FastEthernet0/0.806
encapsulation dot1Q 806
ip address 10.75.152.1 255.255.254.0
```

---

## 5. Static Routing Table

Terminal 5's router (model 2811) is connected to the Campus Backbone via IP `10.75.208.5`

To reach the networks of the other terminals and the Internet, the following static routes were configured:

| Destination Network (IP Block) |     Mask      | Next-Hop<br/>(IP of the Destination Router on the Backbone) |             Description              |
|:------------------------------:|:-------------:|:-----------------------------------------------------------:|:------------------------------------:|
|          10.75.160.0           | 255.255.240.0 |                         10.75.208.2                         |         Route to Terminal 2          |
|          10.75.192.0           | 255.255.240.0 |                         10.75.208.4                         |         Route to Terminal 4          |
|          10.75.176.0           | 255.255.240.0 |                         10.75.208.3                         |         Route to Terminal 3          |
|            0.0.0.0             |    0.0.0.0    |                         10.75.208.2                         | Standard Route for Internet (via T2) |