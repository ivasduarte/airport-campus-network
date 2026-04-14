# Terminal 2

---

## IPv4 Networking

**Terminal defined IPv4 addresses:** 

---

### Terminal required nodes

**User outlets:** 1000 nodes <br> 
**Wi-Fi:** 2000 nodes <br>
**VoIP:** 500 nodes <br>
**Servers DMZ:** 100 nodes <br>

### IPv4 Network Block

During the planning meeting it was decided that the address block for this terminal is: **10.75.160.0 /20**.

Knowing that, we can divide this block into 4 different ones:
1. **User Outlets** → 10.75.168.0 /22
2. **Wi-Fi** → 10.75.160.0 /21
3. **VoIP** → 10.75.172.0 /23
4. **Servers DMZ** → 10.75.174.0 /25

Each of the above IPv4 networks will be associated with the respective VLAN. <br>
* **e.g.:** VLANID = 799 → 10.75.168.0 /22 → User Outlets 

---

## Static Routing