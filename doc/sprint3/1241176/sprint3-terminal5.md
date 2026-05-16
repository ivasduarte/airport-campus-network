RCOMP 2025-2026: Project 1 Sprint 3 Member 1241176
=====

### Contents

1. [Dynamic Routing (OSPF)](#1-dynamic-routing-ospf)
   - [Advertised Networks](#11-advertised-networks)
2. [Local DNS and HTTP Services](#2-local-dns-and-http-services)
   - [HTTP Server Setup (DMZ)](#21-http-server-setup-dmz)
   - [DNS Resource Records](#22-dns-resource-records)
3. [VoIP Service Configuration](#3-voip-service-configuration)
    - [Switch Ports for IP Phones](#31-switch-ports-for-ip-phones)
4. [Static NAT Configuration](#4-static-nat-configuration)
   - [Port Forwarding Rules](#41-port-forwarding-rules)
5. [Static Firewall (ACLs)](#5-static-firewall-acls)
   - [Access Control Lists Strategy](#51-access-control-lists-strategy)


---

## Quick Reference — Terminal 5 VLANs and Networks

| **VLAN** |   **Description**   |   **Network**   | **Gateway**  | **Subnet Mask** |
|:--------:|:-------------------:|:---------------:|:------------:|:---------------:|
|   797    |      Backbone       | 10.75.208.0/24  | 10.75.208.5  |  255.255.255.0  |
|   803    |        Wi-Fi        | 10.75.128.0/20  | 10.75.128.1  |  255.255.240.0  |
|   804    | End Users (Outlets) | 10.75.144.0/21  | 10.75.144.1  |  255.255.248.0  |
|   805    |    DMZ (Servers)    | 10.75.154.0/24  | 10.75.154.1  |  255.255.255.0  |
|   806    |        VoIP         | 10.75.152.0/23  | 10.75.152.1  |  255.255.254.0  |


**DMZ Servers (static addresses):**
- DNS Server (ns): `10.75.154.10` (Already existed from Sprint 2)
- HTTP Server: `10.75.154.11` (New server to be added)

---

## 1. Dynamic Routing (OSPF)

In Sprint 3, the static routing table was removed to implement a dynamic routing protocol (OSPF). 
This ensures dynamic convergence and route exchange between the Campus Backbone and Terminal 5.

* **OSPF Process ID:** 1
* **Router ID:** `10.75.208.5`
* **Backbone Area:** 0 (for Interface Fa0/0.797)
* **Local Terminal Area:** 5 (for Internal Subnets)


### 1.1. Advertised Networks

| **Network** | **Wildcard Mask** | **Area** | **Description**            |
|:-----------:|:-----------------:|:--------:|----------------------------|
| 10.75.208.0 |     0.0.0.255     |    0     | Campus Backbone            |
| 10.75.128.0 |    0.0.15.255     |    5     | T5 Wi-Fi VLAN (803)        |
| 10.75.144.0 |     0.0.7.255     |    5     | T5 User Outlets VLAN (804) |
| 10.75.152.0 |     0.0.1.255     |    5     | T5 VoIP VLAN (806)         |
| 10.75.154.0 |     0.0.0.255     |    5     | T5 DMZ Servers VLAN (805)  |

---

## 2. Local DNS and HTTP Services

A local domain was established for Terminal 5, and a secondary server was added to the DMZ to fulfill the 
HTTP/HTTPS service requirements.

* **Local Domain:** `terminal-5.rcomp-25-26-di-g2`
* **DNS Server IP:** `10.75.154.10`
* **HTTP Server IP:** `10.75.154.11`

### 2.1. HTTP Server Setup (DMZ)

In Packet Tracer, add a new Server-PT to the DMZ network (VLAN 805) and connect it to the DMZ switch (HC of L01 or L02). 
Set the following static IP parameters:

* **IP:** `10.75.154.11`
* **Mask:** `255.255.255.0`
* **Gateway:** `10.75.154.1`
* **DNS:** `10.75.154.10`
* **Default Domain:** `terminal-5.rcomp-25-26-di-g2`
  
Under the Services → HTTP tab, enable HTTP and HTTPS. Edit the index.html page to identify the terminal:

```
<html>
<body>
<h1>Terminal 5 - HTTP Server</h1>
<p>RCOMP 2025-2026 Project 1 - Sprint 3</p>
</body>
</html>
```

_Note: Ensure HTTP/HTTPS is also enabled on the DNS Server (10.75.154.10) with a similar HTML page, 
as NAT will redirect external HTTP/HTTPS traffic there._


### 2.2. DNS Resource Records

On the DNS Server (10.75.154.10), under the Services → DNS tab, enable the service and add the following records:

| **Number** |           **Name (FQDN)**            | **Type**  |              **Detail**              |
|:----------:|:------------------------------------:|:---------:|:------------------------------------:|
|     0      |   dns.terminal-5.rcomp-25-26-di-g2   |   CNAME   |   ns.terminal-5.rcomp-25-26-di-g2    |
|     1      |   ns.terminal-5.rcomp-25-26-di-g2    | A Record  |             10.75.154.10             |
|     2      | server.terminal-5.rcomp-25-26-di-g2  | A Record  |             10.75.154.11             |
|     3      |     terminal-5.rcomp-25-26-di-g2     | A Record  |             10.75.154.10             |
|     4      |   web.terminal-5.rcomp-25-26-di-g2   |   CNAME   | server.terminal-5.rcomp-25-26-di-g2  |
|     5      |   www.terminal-5.rcomp-25-26-di-g2   |   CNAME   | server.terminal-5.rcomp-25-26-di-g2  |
|     6      |          rcomp-25-26-di-g2           | A Record  |             10.75.174.2              |
|     7      |          rcomp-25-26-di-g2           |    NS     |          rcomp-25-26-di-g2           |


(Records 6 and 7 are mandatory — they point to the root DNS server of Terminal 2 (10.75.174.2), which acts as the 
parent domain. All DNS servers across the terminals need to be aware of the root server).

---

## 3. VoIP Service Configuration

The Cisco IP Telephony service was established for Terminal 5. The router acts as the Unified Communications Manager Express (CME).

* **VLAN ID:** 806
* **Network:** 10.75.152.0/23
* **Default Router (Gateway):** 10.75.152.1
* **TFTP Server (Option 150):** 10.75.152.1
* **Terminal Prefix:** 5 (Valid Range: 5***)


### 3.1. Switch Ports for IP Phones

On the HC switches (L01-HC1 and L02-HC1), the ports connected to the 7960 IP phones require the following configuration:

```
interface GigabitEthernet4/1
 no switchport access vlan
 switchport mode access
 switchport voice vlan 806
```

In Packet Tracer, add two 7960 IP Phones — one to each HC switch. 
The extensions 5001 and 5002 should be assigned automatically upon registration.

---

## 4. Static NAT Configuration

To allow external access to the internal web services of Terminal 5 without exposing the private IP addressing 
of the DMZ, a Static NAT (Port Forwarding) was configured on the Router.

* **Inside Interface:** Fa0/0.803, Fa0/0.804, Fa0/0.805, Fa0/0.806
* **Outside Interface:** Fa0/0.797 (Backbone)


### 4.1. Port Forwarding Rules

| External IP (Outside) | External Port | Internal IP (Inside) | Internal Port | Protocol | Target Service |
|:---------------------:|:-------------:|:--------------------:|:-------------:|:--------:|:--------------:|
|      10.75.208.5      |      80       |     10.75.154.10     |      80       |   TCP    |      HTTP      |
|      10.75.208.5      |      443      |     10.75.154.10     |      443      |   TCP    |     HTTPS      |


---

## 5. Static Firewall (ACLs)

Traffic access policies were implemented using Extended Access Control Lists (ACLs) applied to the router's 
subinterfaces. The configuration strictly follows the 5 rules of precedence required for Sprint 3.


### 5.1. Access Control Lists Strategy

| Precedence Rule             | Security Policy Description                                                                                                          | Implemented In |
|:----------------------------|:-------------------------------------------------------------------------------------------------------------------------------------|:---------------|
| **1st - Anti-Spoofing**     | Blocks internal T5 IPs arriving from the external backbone.                                                                          | `BACKBONE_IN`  |
| **2nd - ICMP Permitted**    | Echo requests and echo replies are always permitted.                                                                                 | *All ACLs*     |
| **3rd - DMZ Protection**    | Blocks all traffic to the DMZ except DNS (.10) and HTTP/HTTPS (.10 and .11). Traffic originating FROM the DMZ is permitted.          | `DMZ_OUT`      |
| **4th - Router Protection** | Blocks traffic directed to the router itself, excepting required services (DHCP, TFTP, SCCP on port 2000, OSPF, and NAT HTTP/HTTPS). | `ROUTER_IN`    |
| **5th - Pass-Through**      | The rest passes. General cross-network transit traffic is permitted.                                                                 | *All ACLs*     |