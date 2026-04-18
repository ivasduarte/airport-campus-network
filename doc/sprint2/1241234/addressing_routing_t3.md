RCOMP 2025-2026: Project 1 Sprint 2 Member 1241234 File
=====

### Contents

1. [Network Base Data](#1-network-base-data)
2. [Subnetting (VLSM)](#2-subnetting-vlsm)
    - [Wi-Fi VLAN](#21-wi-fi-vlan-t3vlan811)
    - [User Outlets VLAN](#22-user-outlets-vlan-t3vlan812)
    - [VoIP VLAN](#23-voip-vlan-t3vlan813)
    - [DMZ Servers VLAN](#24-dmz-servers-vlan-t3vlan814)
3. [IP Address Assignment](#3-ip-address-assignment-end-devices-and-interfaces)
4. [Static Routing Table](#4-static-routing-table)

---

## 1. Network Base Data

According to the team planning meeting, the following parameters were defined for Terminal 3:
* **IPv4 Block Assigned to Terminal 3:** 10.75.176.0/20
* **VLAN IDs Assigned:** 811 to 814
* **Campus Backbone Network:** 10.75.208.0/24
* **DMZ Switch Network:** 10.75.210.0/23

---

## 2. Subnetting (VLSM)

To accommodate the node requirements of Terminal 3, the block ´10.75.176.0/20` was subdivided from the largest network to the smallest:

### 2.1. Wi-Fi VLAN (T3VLAN811)
* **Requirement:** 1500 nodes
* **Required Size:** 2048 usable IPs → /21 mask
* **Network Address:** 10.75.176.0/21
* **First Usable IP (Gateway):** 10.75.176.1
* **Last Usable IP:** 10.75.183.254
* **Broadcast Address:** 10.75.183.255
* **Subnet Mask:** 255.255.248.0


### 2.2. User Outlets VLAN (T3VLAN812)
* **Requirement:** 950 nodes
* **Required Size:** 1024 usable IPs → /22 mask
* **Network Address:** 10.75.184.0/22
* **First Usable IP (Gateway):** 10.75.184.1
* **Last Usable IP:** 10.75.187.254
* **Broadcast Address:** 10.75.187.255
* **Subnet Mask:** 255.255.252.0


### 2.3. VoIP VLAN (T3VLAN813)
* **Requirement:** 350 nodes
* **Required Size:** 512 usable IPs → /23 mask
* **Network Address:** 10.75.188.0/23
* **First Usable IP (Gateway):** 10.75.188.1
* **Last Usable IP:** 10.75.189.254
* **Broadcast Address:** 10.75.189.255
* **Subnet Mask:** 255.255.254.0


### 2.4. DMZ Servers VLAN (T3VLAN814)
* **Requirement:** 150 nodes
* **Required Size:** 256 usable IPs → /24 mask
* **Network Address:** 10.75.190.0/24
* **First Usable IP (Gateway):** 10.75.190.1
* **Last Usable IP:** 10.75.190.254
* **Broadcast Address:** 10.75.190.255
* **Subnet Mask:** 255.255.255.0

---

## 3. IP Address Assignment (End Devices and Interfaces)

To ensure that the networks are functional in the Packet Tracer simulation, the following IPs were statically configured 
on the test devices:

|     **Device**      | **VLAN** |         **Device IP**          | **Subnet Mask** | **Default Gateway** |
|:-------------------:|:--------:|:------------------------------:|:---------------:|:-------------------:|
|  **Access Point**   |   812    |          10.75.128.x           |  255.255.240.0  |     10.75.128.1     |
|  **PC (Outlets)**   |   811    |          10.75.144.x           |  255.255.248.0  |     10.75.144.1     |
|    **PC (DMZ)**     |   798    |          10.75.210.x           |  255.255.254.0  |       0.0.0.0       |
|     **Server**      |   814    |          10.75.154.x           |  255.255.255.0  |     10.75.154.1     |
| **IP Phone (VoIP)** |   813    | Configure via DHCP in Sprint 3 |        -        |          -          |

### Router T4 Subinterfaces

| Subinterface | VLAN |     IP      |      Mask       |
|:------------:|:----:|:-----------:|:---------------:|
|  Fa0/0.797   | 797  | 10.75.208.3 |  255.255.255.0  |
|  Fa0/0.811   | 811  | 10.75.184.1 |  255.255.252.0  |
|  Fa0/0.812   | 812  | 10.75.176.1 |  255.255.248.0  |
|  Fa0/0.813   | 813  | 10.75.188.1 |  255.255.254.0  |
|  Fa0/0.814   | 814  | 10.75.190.1 |  255.255.255.0  |

### Switch Management IPs (Switches DMZ – VLAN 798)

|  Switch  |      IP      |     Mask      |
|:--------:|:------------:|:-------------:|
|  T4-MC   | 10.75.210.16 | 255.255.254.0 |
| T4-IC-L0 | 10.75.210.17 | 255.255.254.0 |
| T4-IC-L2 | 10.75.210.18 | 255.255.254.0 |
| T4-HC-L0 | 10.75.210.19 | 255.255.254.0 |
| T4-HC-L2 | 10.75.210.20 | 255.255.254.0 |

---

## 4. Switches Configuration (VLAN 798)

A switch management zone (DMZ) is a dedicated and isolated network, without a router/gateway. 

- **Switch Configuration:** The VLAN 798 must be created on each switch and assigned an IP address.

### 4.1. Sub-Interfaces

The router (model 2811) will be the "Default Gateway" for VLANs 811, 812, 813, and 814. The connection from the router
to the main switch (main cross-connect) must be made on a port in *Trunk Mode*. 

```
// for Wi-Fi VLAN
interface FastEthernet0/0.812
encapsulation dot1Q 812
ip address 10.75.176.1 255.255.248.0

// for user outlets VLAN
interface FastEthernet0/0.811
encapsulation dot1Q 811
ip address 10.75.184.1 255.255.252.0

// for servers VLAN
interface FastEthernet0/0.814
encapsulation dot1Q 814
ip address 10.75.190.1 255.255.255.0

// for VoIP VLAN
interface FastEthernet0/0.813
encapsulation dot1Q 813
ip address 10.75.188.1 255.255.254.0
```

---

## 5. Static Routing Table

Terminal 3's router (model 2811) is connected to the Campus Backbone via IP `10.75.208.3`

To reach the networks of the other terminals and the Internet, the following static routes were configured:

| Destination Network (IP Block) |     Mask      | Next-Hop<br/>(IP of the Destination Router on the Backbone) |             Description              |
|:------------------------------:|:-------------:|:-----------------------------------------------------------:|:------------------------------------:|
|          10.75.160.0           | 255.255.240.0 |                         10.75.208.2                         |         Route to Terminal 2          |
|          10.75.192.0           | 255.255.240.0 |                         10.75.208.4                         |         Route to Terminal 4          |
|          10.75.128.0           | 255.255.240.0 |                         10.75.208.5                         |         Route to Terminal 5          |
|            0.0.0.0             |    0.0.0.0    |                         10.75.208.2                         | Standard Route for Internet (via T2) |