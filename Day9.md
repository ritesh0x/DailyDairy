# 🔖 Day 9: IP Addressing, MAC, and Subnetting Fundamentals

**🗓️ Date:** June 27, 2025

---

### 🧠 Topics Covered:

* IP Address and its structure
* Types of IP addresses (Public, Private, Static, Dynamic)
* MAC Address and its significance
* Subnetting basics
* Classful addressing
* Classless addressing (CIDR)

---

### 💻 What I Did:

Today I studied the fundamental concepts of networking, specifically focusing on **IP addressing**, **MAC addresses**, and **subnetting**. I explored both **classful** and **classless** addressing systems to understand how networks are organized and subdivided. These concepts are essential for network planning, routing, and security.

---

### 📡 IP Address:

* An **IP address** is a unique identifier assigned to each device on a network.
* It consists of two parts: **Network ID** and **Host ID**.
* Written in **IPv4** format as 4 decimal numbers (e.g., 192.168.1.1).

#### 🧾 Types of IP Addresses:

* **Public IP**: Routable on the internet (assigned by ISPs)
* **Private IP**: Used within internal networks (e.g., 192.168.x.x)
* **Static IP**: Manually assigned, does not change
* **Dynamic IP**: Assigned by DHCP server, changes periodically

---

### 🔗 MAC Address:

* Stands for **Media Access Control Address**
* A hardware address burned into the network interface card (NIC)
* Uniquely identifies each device at the data link layer
* Format: `00:1A:2B:3C:4D:5E`

---

### 🔄 Subnetting:

* Process of dividing a larger network into smaller, manageable sub-networks (subnets)
* Helps improve **network performance** and **security**
* Uses **subnet masks** to define boundaries (e.g., 255.255.255.0)

---

### 🗂️ Classful Addressing:

| Class | Starting Bits | Range                       | Default Subnet Mask |
| ----- | ------------- | --------------------------- | ------------------- |
| A     | 0             | 1.0.0.0 – 126.255.255.255   | 255.0.0.0           |
| B     | 10            | 128.0.0.0 – 191.255.255.255 | 255.255.0.0         |
| C     | 110           | 192.0.0.0 – 223.255.255.255 | 255.255.255.0       |

---

### 📉 Classless Addressing (CIDR):

* **CIDR (Classless Inter-Domain Routing)** removes the fixed boundaries of classful addressing
* Example: `192.168.1.0/24` (means 24 bits for network, rest for hosts)
* Allows efficient IP allocation and routing

---

### 🧠 Key Learnings:

* IP and MAC addresses are fundamental to device identification and communication
* Subnetting is critical for segmenting and securing large networks
* Classful addressing is outdated but useful for understanding the basics
* CIDR allows more flexibility in subnetting and IP address allocation

---

[⬅️ Back to Day 8](Day8.md) | [➡️ Go to Day 10](Day10.md)
