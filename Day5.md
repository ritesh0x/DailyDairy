# 🔖 Day 5: Android Hacking with ADB and Vysor

**🗓️ Date:** June 23, 2025

---

### 🧠 Topics Covered:

* ADB (Android Debug Bridge) setup and commands
* Connecting Android to PC over WiFi using TCP/IP
* File transfer using `push` and `pull` commands
* Exploring the Android shell via terminal
* Screen mirroring using **Vysor**
* Developer options and USB debugging in Android

---

### 💻 What I Did:

Today I learned how to access and control an Android device from a PC using **ADB commands**, and how to perform basic file transfers. I also used **Vysor** for Android screen mirroring.

---

### ⚡ Prerequisites:

1. A Windows laptop and an Android phone
2. Both devices connected to the **same WiFi network**
3. Downloaded and extracted **Android SDK Platform Tools** (ADB tools) for Windows

---

### ⚖️ Setup Process:

#### 1. **Enable Developer Options**

* Go to **Settings > About Phone**
* Tap **Build Number** 5–7 times
* Now go to **Settings > Additional Settings > Developer Options**
* Enable **USB Debugging**

#### 2. **Prepare Platform Tools**

* Go to the folder where you extracted **platform-tools**
* Open a terminal in that folder (Shift + Right-click > Open in Terminal)

#### 3. **Connect the Phone**

* Use USB cable and select **File Transfer** mode on phone
* In terminal, run:

  ```bash
  ./adb devices
  ```
* Allow the connection when the phone prompts for authorization

#### 4. **Connect Over WiFi**

* Run the following to switch to TCP/IP mode:

  ```bash
  ./adb tcpip 5555
  ```
* Get your phone’s IP address (from WiFi settings)
* Connect to your phone:

  ```bash
  ./adb connect 192.168.1.39:5555
  ```
* Now **you can unplug the USB cable**

---

### 💡 Useful ADB Commands:

| Command                          | Description                        |
| -------------------------------- | ---------------------------------- |
| `./adb devices`                  | Shows connected devices            |
| `./adb shell`                    | Opens the Android shell (terminal) |
| `./adb pull /path/on/phone`      | Downloads file from phone to PC    |
| `./adb push file /path/on/phone` | Uploads file from PC to phone      |

---

### 📱 Android Screen Mirroring using Vysor:

* Used **Vysor** to remotely control Android from the PC
* It mirrors your phone's screen and allows interaction via mouse and keyboard

---

### 🧠 Key Learnings:

* USB debugging allows full terminal control of an Android device
* ADB can be used to access files, install apps, and interact with Android shell
* WiFi connection allows wireless Android access
* Vysor simplifies control and testing for mobile security

---

### 🛠️ Tools Used:

* **ADB (Platform Tools)**
* **Android phone with Developer Mode**
* **Vysor** for screen mirroring
* **Kali Linux/Windows terminal**

---

[⬅️ Back to Day 4](Day4.md) | [➡️ Go to Day 6](Day6.md)
