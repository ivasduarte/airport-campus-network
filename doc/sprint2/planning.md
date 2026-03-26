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

* **Packet Tracer Version:** All team members must use **Cisco Packet Tracer version 9.0.0.810**.

* **VLANIDs and corresponding VLAN names:** 
  * The VLANIDs range assigned to our group was: **797-817**.  
  * As our team is composed by four team members, we decidedd to make the following distribution:
    * **Campus Backbone :** VLANID = 797
    * **Switches DMZ :** VLANID = 798
    * **1241166 :** VLANID = 799-802
    * **1241176 :** VLANID = 803-806
    * **1241229 :** VLANID = 807-810
    * **1241234 :** VLANID = 811-814
    * _The VLANIDs 815-817 are free to use, at the moment of the planning meeting._
  * For the name of the VLANs we decided to follow the rules below:
    * T$x$VLAN$ID$
      * $x$ → Terminal where the VLAN will be used.
      * $ID$ → ID assigned to the VLAN. 

* **Default VLAN:** For the default VLAN we decided to keep the VLANID = 1.

* **VTP Domain name:** rc2526dig2

* **IPv4 network addresses for Campus Backbone and Switches DMZ network:**
  * **Campus Backbone :** 10.75.195.0 /24
  * **Switches DMZ Network :** 10.75.194.0 /23

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