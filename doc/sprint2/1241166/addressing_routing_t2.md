# RCOMP 2025-2026: Project 1 Sprint 2 Member 1221166 File

---

## IPv4 Networking

### 1. Terminal required nodes

**User outlets:** 1000 nodes <br>
**Wi-Fi:** 2000 nodes <br>
**VoIP:** 500 nodes <br>
**Servers DMZ:** 100 nodes <br>

### 2. IPv4 Network Block

During the planning meeting it was decided that the address block for this terminal is: **10.75.160.0 /20**.

Knowing that, we can divide this block into 4 different ones:

1. **User Outlets** → 10.75.168.0 /22
2. **Wi-Fi** → 10.75.160.0 /21
3. **VoIP** → 10.75.172.0 /23
4. **Servers DMZ** → 10.75.174.0 /25

Each of the above IPv4 networks will be associated with the respective VLAN. <br>

* **e.g.:** VLANID = 799 → 10.75.168.0 /22 → User Outlets

---

## 3. Static Routing

Terminal 2's router (model 2811) is connected to the Campus Backbone via IP `10.75.208.2`

To reach the networks of the other terminals and the Internet, the following static routes were configured:

| Destination Network (IP Block) |     Mask      | Next-Hop<br/>(IP of the Destination Router on the Backbone) |        Description         |
|:------------------------------:|:-------------:|:-----------------------------------------------------------:|:--------------------------:|
|          10.75.176.0           | 255.255.240.0 |                         10.75.208.3                         |    Route to Terminal 3     |
|          10.75.192.0           | 255.255.240.0 |                         10.75.208.4                         |    Route to Terminal 4     |
|          10.75.128.0           | 255.255.224.0 |                         10.75.208.5                         |    Route to Terminal 5     |
|            0.0.0.0             |    0.0.0.0    |                        89.73.67.230                         | Default Route → ISP Router |