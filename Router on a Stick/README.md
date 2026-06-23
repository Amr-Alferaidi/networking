


# Router on a Stick

## 📖 Overview
This project demonstrates inter-VLAN routing using a single router interface.

## 🧠 Concepts
- VLANs
- Trunking
- Subinterfaces

## 🖥️ Topology
<img width="1366" height="768" alt="Screenshot (25)" src="https://github.com/user-attachments/assets/9a4c3bfa-9e23-4521-8db5-56290fb14a9e" />

ports 
<img width="687" height="410" alt="Ports and Description" src="https://github.com/user-attachments/assets/2da9814d-379f-44c3-9e07-58545a7788b6" />

## ⚙️ Configuration
Switch Configuration
VLANs created: 10, 20, 30
Access ports assigned to respective VLANs
<img width="649" height="261" alt="Vlans" src="https://github.com/user-attachments/assets/cda91662-9adf-4690-aacc-3548756a5eaf" />
Trunk port configured between switch and router
Allowed VLANs: 10, 20, 30
<img width="564" height="187" alt="Trunk" src="https://github.com/user-attachments/assets/619dc9f3-dea3-4e2f-af73-4a16ea4b9354" />

 Router-on-a-Stick Configuration
Sub interfaces configured on a single router interface:
interface g0/1.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
interface g0/1.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0
interface g0/1.30
 encapsulation dot1Q 30
 ip address 192.168.30.1 255.255.255.0
 <img width="654" height="137" alt="Router on stick" src="https://github.com/user-attachments/assets/84a2e5d1-69b4-4f70-975e-f79910dc5726" />

<img width="690" height="140" alt="DHCP" src="https://github.com/user-attachments/assets/0c221434-eb08-41d7-abb0-8f1474c7517b" />

<img width="364" height="165" alt="Router on stick 2" src="https://github.com/user-attachments/assets/edaf25ee-9a9f-4981-bd3a-b7947f050572" />

   DHCP Configuration
•	DHCP configured on the router for each VLAN
•	Automatic IP assignment for IT and HR devices
•	Default gateway assigned per VLAN
<img width="355" height="250" alt="DHCP configuration" src="https://github.com/user-attachments/assets/c0da4819-4b67-4ec6-a852-6e795802f33d" />

<img width="690" height="140" alt="DHCP" src="https://github.com/user-attachments/assets/ce64727a-bc2a-4110-a03c-e8c968530e21" />


##Results
<img width="1366" height="768" alt="HR ping" src="https://github.com/user-attachments/assets/db95d24d-d25e-4492-a898-0dd7917f5b6a" />
<img width="1366" height="768" alt="IT ping" src="https://github.com/user-attachments/assets/eac28c80-bed4-4650-9c6e-befecdeeeb4c" />

##troubleshooting 
Printer don't have dainamic IP 
<img width="1366" height="768" alt="trubleshoting DHCP Print not working" src="https://github.com/user-attachments/assets/88cc88c4-022a-4968-a561-cdf2acd42c55" />

investigating 
<img width="683" height="607" alt="invistigating" src="https://github.com/user-attachments/assets/95b6ec28-b959-44c0-8aba-554659f00fc7" />

solving
<img width="643" height="136" alt="solving" src="https://github.com/user-attachments/assets/36d12087-787e-4b85-9960-40c3f86e698a" />

solved 
<img width="930" height="332" alt="solved" src="https://github.com/user-attachments/assets/950d9e7c-6dfd-47ea-8de4-4bd47f967c2d" />

