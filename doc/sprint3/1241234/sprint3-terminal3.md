# RCOMP 2025-2026: Project 1 Sprint 3 Member 1241234

=====

### Contents

1. [Dynamic Routing (OSPF)](#1-dynamic-routing-ospf)
2. [Local DNS and HTTP Services](#2-local-dns-and-http-services)
3. [VoIP Service Configuration](#3-voip-service-configuration)
4. [Static NAT Configuration](#4-static-nat-configuration)
5. [Static Firewall (ACLs)](#5-static-firewall-acls)

---

## 1. Dynamic Routing (OSPF)

In Sprint 3, the previous static routing approach was replaced by dynamic routing using OSPF. This allows Terminal 3 to exchange routes dynamically with the Campus Backbone and with the remaining terminals after integration.

* **OSPF Process ID:** 1
* **Router ID:** 3.3.3.3
* **Backbone Area:** 0 (for Interface Fa0/0.797)
* **Local Terminal Area:** 3 (for Terminal 3 internal subnets)

### 1.1. Advertised Networks

| Network Address | Wildcard Mask | Area |          Description          |
|:---------------:|:-------------:|:----:|:-----------------------------:|
|   10.75.208.0   |   0.0.0.255   |  0   |       Campus Backbone         |
|   10.75.176.0   |   0.0.7.255   |  3   |     T3 Wi-Fi VLAN (812)       |
|   10.75.184.0   |   0.0.3.255   |  3   | T3 User Outlets VLAN (811)    |
|   10.75.188.0   |   0.0.1.255   |  3   |     T3 VoIP VLAN (813)        |
|   10.75.190.0   |   0.0.0.255   |  3   | T3 DMZ Servers VLAN (814)     |

---

## 2. Local DNS and HTTP Services

A local DNS domain was established for Terminal 3. The first server in the DMZ is used as the local DNS server and also provides HTTP/HTTPS services. A second server was added to the DMZ to provide the required HTTP/HTTPS web service.

* **Local Domain:** `terminal-3.rcomp-25-26-di-g2`
* **DNS Server IP:** 10.75.190.2
* **HTTP Server IP:** 10.75.190.3
* **DMZ Gateway:** 10.75.190.1
* **DMZ VLAN:** 814

### 2.1. DNS Resource Records

The DNS database configured on the Terminal 3 name server contains the following records:

| Name | Type | Value |
|:-----|:----:|:------|
| `ns.terminal-3.rcomp-25-26-di-g2` | A | `10.75.190.2` |
| `server1.terminal-3.rcomp-25-26-di-g2` | A | `10.75.190.3` |
| `www.terminal-3.rcomp-25-26-di-g2` | CNAME | `server1.terminal-3.rcomp-25-26-di-g2` |
| `web.terminal-3.rcomp-25-26-di-g2` | CNAME | `server1.terminal-3.rcomp-25-26-di-g2` |
| `dns.terminal-3.rcomp-25-26-di-g2` | CNAME | `ns.terminal-3.rcomp-25-26-di-g2` |
| `terminal-3.rcomp-25-26-di-g2` | NS | `ns.terminal-3.rcomp-25-26-di-g2` |
| `rcomp-25-26-di-g2` | NS | `ns.rcomp-25-26-di-g2` |
| `ns.rcomp-25-26-di-g2` | A | `10.75.174.2` |

---

## 3. VoIP Service Configuration

The Cisco IP Telephony service was established for Terminal 3. The router acts as the Unified Communications Manager Express (CME) and provides local telephony services for the IP phones in the VoIP VLAN.

* **VLAN ID:** 813
* **Network:** 10.75.188.0/23
* **Default Router (Gateway):** 10.75.188.1
* **TFTP Server (Option 150):** 10.75.188.1
* **Terminal Prefix:** 3 (Valid Range: 3***)
* **Local Phone Numbers:** 3001 and 3002
* **Switchport Configuration:** Ports connected to IP phones have the access VLAN disabled and the voice VLAN 813 enabled.
* **Call Forwarding:** Dial-peers configured to forward calls to Terminals 2, 4, and 5.

---

### 3.1. DHCPv4 Service

The router provides DHCPv4 for the internal Terminal 3 networks, except for the backbone and DMZ networks, where addressing is static.

| DHCP Pool | Network | Default Router | DNS Server | Additional Option |
|:---------:|:-------:|:--------------:|:----------:|:-----------------:|
| `T3-WIFI` | `10.75.176.0/21` | `10.75.176.1` | `10.75.190.2` | Domain name configured |
| `T3-USERS` | `10.75.184.0/22` | `10.75.184.1` | `10.75.190.2` | Domain name configured |
| `T3-VOIP` | `10.75.188.0/23` | `10.75.188.1` | `10.75.190.2` | Option 150: `10.75.188.1` |

---

## 4. NAT Configuration

To allow access from the Campus Backbone to the internal HTTP/HTTPS service of Terminal 3 without directly exposing the DMZ addressing, Static NAT (Port Forwarding) was configured on the router.

* **Inside Interface:** Fa0/0.814 (DMZ)
* **Outside Interface:** Fa0/0.797 (Backbone)

### 4.1. Port Forwarding Rules

| External IP (Outside) | External Port | Internal IP (Inside) | Internal Port | Protocol | Target Service |
|:---------------------:|:-------------:|:--------------------:|:-------------:|:--------:|:--------------:|
|      10.75.208.3      |      80       |     10.75.190.2      |      80       |   TCP    |      HTTP      |
|      10.75.208.3      |      443      |     10.75.190.2      |      443      |   TCP    |     HTTPS      |

---

## 5. Static Firewall (ACLs)

Traffic access policies were implemented using Extended Access Control Lists (ACLs) applied to the router's subinterfaces. The ACLs follow the required Sprint 3 policy order: anti-spoofing, ICMP permission, DMZ protection, router protection, and pass-through traffic permission.

### 5.1. Access Control Lists Strategy

| Precedence Rule             | Security Policy Description                                                                                                           | Implemented In |
|:----------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|:---------------|
| **1st - Anti-Spoofing**     | Blocks traffic arriving from the external backbone while pretending to originate from Terminal 3 local networks.                       | `T3-BACKBONE-IN` |
| **2nd - ICMP Permitted**    | Echo requests and echo replies are permitted.                                                                                         | *All ACLs* |
| **3rd - DMZ Protection**    | Blocks all traffic to the DMZ except DNS and HTTP/HTTPS services to the corresponding servers. Traffic originating from the DMZ is permitted. | `T3-BACKBONE-IN`, `T3-USERS-IN`, `T3-WIFI-IN`, `T3-VOIP-IN` |
| **4th - Router Protection** | Blocks traffic directed to the router itself, except required services such as DHCP, TFTP, SCCP/ITS on TCP 2000, OSPF, and NAT HTTP/HTTPS. | `T3-BACKBONE-IN`, `T3-USERS-IN`, `T3-WIFI-IN`, `T3-VOIP-IN` |
| **5th - Pass-Through**      | Remaining transit traffic is permitted.                                                                                               | *All ACLs* |

### 5.2. Interfaces Application

To enforce the strategy above, the ACLs were applied to the following subinterfaces:

* **`T3-BACKBONE-IN`:** Applied on **Fa0/0.797** (Direction: **IN**).
* **`T3-USERS-IN`:** Applied on **Fa0/0.811** (Direction: **IN**).
* **`T3-WIFI-IN`:** Applied on **Fa0/0.812** (Direction: **IN**).
* **`T3-VOIP-IN`:** Applied on **Fa0/0.813** (Direction: **IN**).

No restrictive ACL was applied on the DMZ interface because the defined policy allows traffic originating from the DMZ. Access to the DMZ is controlled by the ACLs applied on the other inbound interfaces.

### 5.3. Main Permitted Services

| Service | Protocol/Port | Purpose |
|:-------:|:-------------:|:--------|
| OSPF | Protocol 89 | Dynamic routing with the backbone routers |
| ICMP Echo/Echo Reply | ICMP | Connectivity tests |
| DNS | UDP/TCP 53 | Name resolution through `10.75.190.2` |
| HTTP | TCP 80 | Web access to DMZ servers and NAT rule |
| HTTPS | TCP 443 | Secure web access to DMZ servers and NAT rule |
| DHCP | UDP 67/68 | Address assignment to Wi-Fi, Users, and VoIP clients |
| TFTP | UDP 69 | IP phone configuration download |
| SCCP/ITS | TCP 2000 | IP phone registration and control |
