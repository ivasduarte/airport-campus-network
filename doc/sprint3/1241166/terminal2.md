# RCOMP 2025-2026: Project 1 Sprint 3 Member 1241166

### Contents

1. [Dynamic Routing (OSPF)](#1-dynamic-routing-ospf)
2. [Local DNS and HTTP Services](#2-local-dns-and-http-services)
3. [VoIP Service Configuration](#3-voip-service-configuration)
4. [Static NAT Configuration](#4-nat-configuration)
5. [Static Firewall (ACLs)](#5-static-firewall-acls)

---

## 1. Dynamic Routing (OSPF)

In Sprint 3, the static routing table was removed to implement a dynamic routing protocol (OSPF).
This ensures dynamic convergence and route between the Campus Backbone and Terminal 2.

* **OSPF Process ID:** 1
* **Router ID:** 10.75.208.2
* **Backbone Area:** 0 (for Interface Fa0/0.797)
* **Local Terminal Area:** 2 (for Internal Subnets)

### 1.1. Advertised Networks

| Network Address | Wildcard Mask | Area |        Description         |
|:---------------:|:-------------:|:----:|:--------------------------:|
|   10.75.208.0   |   0.0.0.255   |  0   |      Campus Backbone       |
|   10.75.160.0   |   0.0.7.255   |  2   |    T2 Wi-Fi VLAN (800)     |
|   10.75.168.0   |   0.0.3.255   |  2   | T2 User Outlets VLAN (799) |
|   10.75.172.0   |   0.0.1.255   |  2   |     T2 VoIP VLAN (801)     |
|   10.75.174.0   |   0.0.0.127   |  2   | T2 DMZ Servers VLAN (802)  |

---

## 2. Local DNS and HTTP Services

A local domain was established for Terminal 2.

* **Local Domain:** `rcomp-25-26-di-g2`
* **DNS Server IP:** 10.75.174.2
* **HTTP Server IP:** 10.75.174.3

### 2.1. DNS Resource Records

Below is a screenshot showing the configuration of the local domain and records on the DNS server (10.75.174.2):

![DNS Configuration T2](assets/DNS_Table.png)

---

## 3. VoIP Service Configuration

The Cisco IP Telephony service was established for Terminal 2.
The router acts as the Unified Communications Manager Express (CME).

* **VLAN ID:** 801
* **Network:** 10.75.172.0 /23
* **Default Router (Gateway):** 10.75.172.1
* **TFTP Server (Option 150):** 10.75.172.1
* **Terminal Prefix:** 2 (Valid Range: 2***)
* **Switchport Configuration:** Ports connected to IP phones have the access VLAN disabled and the voice VLAN 801
  enabled.
* **Call Forwarding:** Dial-peers configured to forward calls to Terminals 3, 4, and 5.

---

## 4. NAT Configuration

To allow external access to the internal web services of Terminal 2 without exposing the private IP addressing of the
DMZ,
a Static NAT (Port Forwarding) was configured on the Router.

* **Inside Interface:** Fa0/0.802 (DMZ)
* **Outside Interface:** Fa0/0.797 (Backbone)

### 4.1. Port Forwarding Rules

| External IP (Outside) | External Port | Internal IP (Inside) | Internal Port | Protocol | Target Service |
|:---------------------:|:-------------:|:--------------------:|:-------------:|:--------:|:--------------:|
|      10.75.208.2      |      80       |     10.75.174.2      |      80       |   TCP    |      HTTP      |
|      10.75.208.2      |      443      |     10.75.174.2      |      443      |   TCP    |     HTTPS      |

---

## 5. Static Firewall (ACLs)

Traffic access policies were implemented using Extended Access Control Lists (ACLs) applied to the router's subinterfaces. 
The configuration strictly follows the 5 rules of precedence required for the Sprint 3.

### 5.1. Interfaces Application

To enforce the strategy above, the ACLs were applied to the following subinterfaces:

* **`BACKBONE_IN`:** Applied on **Fa0/0.797** (Direction: **IN**).
* **`DMZ_OUT`:** Applied on **Fa0/0.802** (Direction: **OUT**).
* **`DMZ_IN`:** Applied on **Fa0/0.802** (Direction: **IN**).
* **`ROUTER_IN`:** Applied on **Fa0/0.799**, **Fa0/0.800** (Direction: **IN**).
* **`VOIP_IN`:** Applied on **Fa0/0.801** (Direction: **IN**)