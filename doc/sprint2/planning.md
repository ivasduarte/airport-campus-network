# RCOMP 2025-2026: Project 1 - Sprint 2 Planning

---

### Sprint Master: 1241166

---

## 1. Sprint's Backlog

- **T.2.1** → Development of a layer two and layer three Packet Tracer simulation for Terminal 2 encompassed floors,
  the campus backbone, and including the internet connection.
- **T.2.2** → Development of a layer two and layer three Packet Tracer simulation for Terminal 3 encompassed floors and
  the campus backbone. Integration of every member's Packet Tracer simulation into a single simulation.
- **T.2.3** → Development of a layer two and layer three Packet Tracer simulation for Terminal 5 encompassed floors and
  the campus backbone.
- **T.2.4** → Development of a layer two and layer three Packet Tracer simulation for Terminal 4 encompassed floors and
  the campus backbone.

---

## 2. Technical Decisions and Coordination

During the team's planning meeting, we agreed on the following technical specifications to ensure consistency across all
terminals:

---

### 2.1. Cisco Packet Tracer version

All team members must use the following version of **Cisco Packet Tracer**: 9.0.0.0810.

---

### 2.2. VLAN Distribution and Naming

Our group have the following range of VLANs assigned: 797-817.

With the group being composed of 4 members, we decided on the following distribution:

* **797** → Campus Backbone
* **798** → Switches DMZ
* **799-802** → 1241166 _(João Ferreira)_
* **803-806** → 1241176 _(Iva Silva)_
* **807-810** → 1241229 _(Diogo Silva)_
* **811-814** → 1241234 _(Gonçalo Tavares)_

> **Note:** The VLAN IDs ranging from 815 to 817 won't be needed.

In order to name all the VLANs we decided to use the following naming rules:

* **VLANs of public use**: These VLANs must be named by its specific use.
    * **797** → _backbone_
    * **798** → _switches_dmz_
* For the rest of the VLANs each team member must use the following format: T$x$VLAN$ID$.
    * $x$ → Terminal responsible for the VLAN
    * $ID$ → ID assigned to the VLAN

> For the **Default VLAN** we decided to keep it as VLANID = 1.
>
> The **VTP Domain Name** assigned to the team was: _rc2526dig2_.

---

### IPv4 Distribution

* **Campus Backbone :** 10.75.208.0 /24
* **Switches DMZ Network :** 10.75.210.0 /23

* **IPv4 network addresses for each team member:**
    * **1241166 :** 10.75.160.0 /20
    * **1241176 :** 10.75.128.0 /19
    * **1241229 :** 10.75.192.0 /20
    * **1241234 :** 10.75.176.0 /20

---

## 3. Subtasks Assignment

* 1241166 → Terminal 2 simulation and internet connection
* 1241176 → Terminal 5 simulation
* 1241229 → Terminal 4 simulation
* 1241234 → Terminal 3 simulation and integration of all simulations in one