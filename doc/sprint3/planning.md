# RCOMP 2025-2026 Project 1 - Sprint 3 planning

---

### Sprint master: 1241229 ###

---

# 1. Sprint's backlog #

* T.3.1 - Update the Terminal2.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for Terminal 2.
* T.3.2 - Update the Terminal3.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for Terminal 3. Final integration of each member's Packet Tracer simulation into a single simulation (campus.pkt).
* T.3.3 - Update the Terminal5.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for Terminal 5.
* T.3.4 - Update the Terminal4.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for Terminal 4.

---

# 2. Technical decisions and coordination #

### OSPF Area IDs ###

The campus network forms a single OSPF autonomous system. Area 0 is reserved for the backbone. Each terminal uses a unique area ID:

| Terminal            | Area ID |
|---------------------|:-------:|
| Backbone (VLAN 797) |    0    |
| Terminal 2          |    2    |
| Terminal 3          |    3    |
| Terminal 4          |    4    |
| Terminal 5          |    5    |

### VoIP phone numbers and prefix digits schema ###

Phone numbers are 4 digits long. The first digit is the prefix and identifies the terminal. Calls are forwarded based on the prefix digit.

| Terminal   | Prefix | Phone numbers |
|------------|:------:|---------------|
| Terminal 2 |   2    | 2001, 2002    |
| Terminal 3 |   3    | 3001, 3002    |
| Terminal 4 |   4    | 4001, 4002    |
| Terminal 5 |   5    | 5001, 5002    |

### DNS domain names ###

The root DNS domain matches the team's repository name: `rcomp-25-26-di-g2` (used in Terminal 2).
All other terminals use subdomains in the format `terminal-X.rcomp-25-26-di-g2`.

### IPv4 node address of the DNS name server of each DNS domain ###

The DNS name server of each terminal is the first server in its DMZ (existing from Sprint 2).
The DNS name server is named `ns` within its domain.

| Terminal   | DNS Domain                     | IP of ns server |
|------------|--------------------------------|:---------------:|
| Terminal 2 | `rcomp-25-26-di-g2`            |   10.75.174.2   |
| Terminal 3 | `terminal-3.rcomp-25-26-di-g2` |   10.75.190.2   |
| Terminal 4 | `terminal-4.rcomp-25-26-di-g2` |   10.75.206.2   |
| Terminal 5 | `terminal-5.rcomp-25-26-di-g2` |  10.75.154.10   |

---

# 3. Subtasks assignment #

* 1241166 - Develop the network simulation for Terminal 2, including the internet connection and OSPF default route origination.
* 1241234 - Develop the network simulation for Terminal 3 and perform the final integration of all members' simulations into campus.pkt.
* 1241176 - Develop the network simulation for Terminal 5.
* 1241229 - Develop the network simulation for Terminal 4.