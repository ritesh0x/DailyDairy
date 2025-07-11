# 🔖 Day 7: Wi-Fi Deauthentication using ESP8266 and wlan0 Adapter

**🗓️ Date:** June 25, 2025

---

### 🧠 Topics Covered:

* Introduction to Wi-Fi deauthentication attacks
* ESP8266 as a deauthentication tool
* Setting up wlan0 interface for packet injection
* Installing drivers for wlan0 compatibility
* Performing Wi-Fi deauthentication attacks using hardware and software

---

### 💻 What I Did:

On Day 7, I learned how to use the **ESP8266 NodeMCU microcontroller** to perform Wi-Fi deauthentication attacks. I also worked on configuring the **wlan0 Wi-Fi adapter** in Kali Linux with the correct drivers to enable **monitor mode** and **packet injection**. These attacks mimic a **denial-of-service (DoS)** condition by disconnecting clients from the target Wi-Fi network.

---

### 🛠️ Tools and Hardware Used:

* **ESP8266 NodeMCU microcontroller**
* **Kali Linux** with terminal access
* **wlan0 Wi-Fi adapter** (monitor mode & packet injection capable)
* **Deauther firmware** / tools like `airmon-ng`, `aireplay-ng`

---

### ✅ Steps Followed:

#### 1. **Prepared the wlan0 Adapter**

* Installed required drivers for monitor mode and packet injection.
* Verified interface status:

  ```bash
  airmon-ng check kill
  airmon-ng start wlan0
  iwconfig
  ```

#### 2. **ESP8266 Setup**

* Flashed the **Wi-Fi Deauther firmware** onto the ESP8266.
* Powered the module and connected to its access point.
* Accessed the ESP8266 **web interface** via browser (default IP: 192.168.4.1).
* Scanned for Wi-Fi networks, selected a target, and launched deauthentication attack.

#### 3. **Wi-Fi Deauthentication (Software Method)**

* Used Kali Linux terminal to perform deauth attacks manually:

  ```bash
  airmon-ng start wlan0
  airodump-ng wlan0mon
  aireplay-ng --deauth 100 -a <router-MAC> wlan0mon
  ```

---

### 🧠 Key Learnings:

* The **ESP8266** is a powerful and affordable tool for wireless testing.
* **Monitor mode** and **packet injection** are essential for Wi-Fi penetration testing.
* **Deauthentication attacks** are useful in testing the resilience of wireless networks.
* These attacks should only be performed on **authorized and legal networks**.
* Installing proper drivers and verifying adapter support is critical for successful wireless testing in Kali Linux.

---

[⬅️ Back to Day 6](Day6.md) | [➡️ Go to Day 8](Day8.md)
