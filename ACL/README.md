#  ACL Network Segmentation

##  Overview
This project demonstrates how to use Extended Access Control Lists (ACLs) to control traffic between different departments in a network.

It is an extension of the Router-on-a-Stick project, adding a security layer to restrict and allow specific communications.

---

##  Network Scenario

- **HR Network:** 192.168.10.0/24  
- **IT Network:** 192.168.20.0/24  
- **Printer:** 192.168.30.2

---

##  Objectives

-  HR can access the Printer  
-  HR cannot access IT network  
-  IT cannot access HR network  
-  IT can access the Printer  

---

## Network Topology

<img width="1366" height="768" alt="Topology" src="https://github.com/user-attachments/assets/9964c954-adfc-4091-9da3-b8541b39acef" />


---

## ⚙️ Configuration

### ACL Configuration

access-list 100 permit ip 192.168.10.0 0.0.0.255 host 192.168.30.2
access-list 100 deny ip 192.168.10.0 0.0.0.255 192.168.20.0 0.0.0.255
access-list 100 permit ip any any


### Apply ACL to Interface
interface g0/1.10
ip access-group 100 in


---

##  Test Results

| Test          | Result | Description            |
|--------------|--------|------------------------|
| HR → IT      | ❌     | Blocked by ACL         |
| HR → Printer | ✅     | Allowed                |
| IT → HR      | ❌     | Implicit deny behavior |
| IT → Printer | ✅     | Allowed                |

<img width="676" height="391" alt="image" src="https://github.com/user-attachments/assets/71e73825-f9ac-4cbb-99bf-3ea3730e288d" />
<img width="679" height="457" alt="image" src="https://github.com/user-attachments/assets/7906d268-1222-4c35-a988-649cec292dd8" />

---

##  Files Included

-  Packet Tracer file (`.pkt`)
-  Network topology image
-  Test results screenshots

---

##  Technologies Used

- Cisco Packet Tracer
- VLANs
- Inter-VLAN Routing
- Extended ACLs

---

##  Author

Amr ALferaidi
