# 🔖 Day 10: Firewall Implementation and SSH/FTP Control

**🗓️ Date:** June 28, 2025

---

### 🧠 Topics Covered:

* Firewall implementation using a Python-based tool
* Managing open ports for security
* Connecting and disconnecting via **SSH (Secure Shell)**
* Connecting and disconnecting via **FTP (File Transfer Protocol)**
* Techniques to identify and close unnecessary open ports

---

### 💻 What I Did:

Today, I implemented a **firewall** using a Python-based network security tool to control access to open ports. I also practiced connecting to remote systems via **SSH** and **FTP**, then learned how to detect and close vulnerable ports to enhance system security.

---

### 🛡️ Firewall Implementation:

* Used a Python tool to:

  * Monitor incoming/outgoing traffic
  * Define allow/deny rules based on ports and IPs
  * Block unauthorized access attempts

* Configured port-blocking rules for unused ports

* Created logs to record connection attempts

---

### 📝 SSH & FTP Management:

* **SSH (Secure Shell):**

  * Used to securely connect to remote systems
  * Practiced login/logout, and tested firewall rules against SSH traffic

* **FTP (File Transfer Protocol):**

  * Used to transfer files over a network
  * Tested access control using firewall settings

---

### 🔌 Closing Open Ports:

* Used tools like `netstat`, `ss`, and `nmap` to detect open ports
* Identified unused or risky ports
* Updated firewall rules to block these ports and verify via scans

---

### 🧠 Key Learnings:

* Firewalls play a critical role in filtering network traffic
* Python scripts can be used for lightweight firewall automation
* SSH and FTP are powerful but must be secured with proper access rules
* Identifying and closing open ports is vital to prevent unauthorized access

---

[⬅️ Back to Day 9](Day9.md) | [➡️ Go to Day 11](Day11.md)
