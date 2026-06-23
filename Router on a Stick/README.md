# Router-on-a-Stick Project

![GitHub repo size](https://img.shields.io/github/repo-size/USERNAME/REPO-NAME?color=blue)
![GitHub last commit](https://img.shields.io/github/last-commit/USERNAME/REPO-NAME?color=green)
![GitHub stars](https://img.shields.io/github/stars/USERNAME/REPO-NAME?style=social)
![GitHub forks](https://img.shields.io/github/forks/USERNAME/REPO-NAME?style=social)

---

## 👨‍💻 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=USERNAME&show_icons=true&theme=tokyonight)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=USERNAME&layout=compact&theme=tokyonight)

---

## 📖 Overview
This project demonstrates **Inter-VLAN Routing (Router-on-a-Stick)** using a single router interface.

---

## 🧠 Key Concepts
- VLANs (Virtual LANs)
- 802.1Q Trunking
- Subinterfaces
- DHCP Configuration
- Inter-VLAN Routing
- Network Troubleshooting

---

## 🖥️ Network Topology

<img width="1366" height="768" alt="Topology" src="https://github.com/user-attachments/assets/9a4c3bfa-9e23-4521-8db5-56290fb14a9c" />

---

## ⚙️ Configuration

### 🔹 VLAN Configuration (Switch)
- VLANs created: 10, 20, 30  
- Ports assigned to correct VLANs  

---

### 🔹 Trunk Configuration
- Link between switch and router configured as trunk  
- Allowed VLANs: 10, 20, 30  

---

### 🔹 Router-on-a-Stick Configuration

```bash
interface g0/1.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0

interface g0/1.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0

interface g0/1.30
 encapsulation dot1Q 30
 ip address 192.168.30.1 255.255.255.0
