# 🔖 Day 3: Phishing Attack using CamPhish & Hack Camera

**🗓️ Date:** June 20, 2025

---

### 🧠 Topics Covered:

* Camera-based phishing attack using **Hack-Camera**
* Using `git clone` to copy tools from GitHub
* Giving script execution permission in Linux
* Launching phishing attacks through the terminal
* Real-world example: capturing webcam images using phishing
* Awareness about **social engineering risks**

---

### 💻 What I Did:

Today I learned how phishing attacks can be executed using **webcam-based lures**. I cloned and executed a tool named **Hack-Camera**, which simulates a fake page asking for camera permission and secretly captures images when users accept.

---

### ⚙️ Steps Performed:

1. **Cloned the Hack-Camera tool**:

   ```bash
   git clone https://github.com/jaspreet-infosec/HACK-CAMERA.git
   ```

2. **Navigated to the tool's folder**:

   ```bash
   cd HACK-CAMERA
   ls
   ```

3. **Switched to root user**:

   ```bash
   sudo su
   ```

4. **Gave execution permission to the script**:

   ```bash
   chmod +x hack_camera.sh
   ```

5. **Ran the script**:

   ```bash
   ./hack_camera.sh
   ```

6. **Selected Option 3 (YouTube Video Phishing)**

7. **Entered YouTube video ID** as prompted

8. **Received phishing link**, opened it in browser

9. **Browser asked for camera access**
   → When granted, it:

   * 🎥 Played the YouTube video to distract the victim
   * 📸 Secretly captured webcam images
   * 📩 Sent images to attacker's terminal
   * 📂 Saved images in the HACK-CAMERA folder

---

### ⚠️ Real-World Implications:

This attack highlights how attackers exploit **trust and curiosity**:

* Users often allow webcam access without thinking
* Phishing pages can be disguised as something innocent like a video
* Images are captured without user knowledge

---

### 🧠 Key Learnings:

* `git clone` helps you download open-source tools from GitHub
* Linux `chmod +x` is used to allow execution of `.sh` files
* Shell scripts can automate complex attacks
* **Social engineering** is one of the most powerful tools in a hacker’s arsenal

---

### 🛠️ Tools Used:

* **Hack-Camera** GitHub tool
* **Linux Terminal (Kali)**
* **Browser** for phishing simulation

---

[⬅️ Back to Day 2](Day2.md) | [➡️ Go to Day 4](Day4.md)
