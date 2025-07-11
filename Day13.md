# 🔖 Day 13: Cryptography and Capture The Flag Challenges

**📅 Date:** July 2, 2025

---

### 🧠 Topics Covered:

* Basics of **Cryptography**
* Hands-on practice with **TryHackMe's Capture the Flag (CTF)** module
* Steganography using **Steghide** and **Spectrogram analysis**
* Concept of **Security Through Obscurity**

---

### 💻 What I Did:

Today, I worked through cryptography-related tasks in the **TryHackMe** platform, especially focusing on **decode/translation** challenges and **file-hiding techniques**. I also explored how **spectrograms** and **Steghide** can hide or reveal hidden data within media files.

---

### 🧩 TryHackMe Module: Capture The Flag

#### 1. 🔡 Translate, Shift, and Decode:

* Given encrypted messages in different formats (e.g., base64, hex, ROT13, Caesar cipher).
* Used the tool **CyberChef** to decode the encrypted text.
* CyberChef auto-detects and decodes formats based on pattern matching.

#### 2. 🎧 Spectrogram-Based Hidden Data:

* Explored how audio files can be used to hide visual messages or text.
* Used **Audacity** (an open-source audio editing tool) to:

  * Open `.wav` or `.mp3` files
  * Switch to spectrogram view
  * Zoom into frequency range to observe hidden images or signals

#### 3. 🖼️ Steghide:

* A command-line tool to hide and extract data from image files.
* **Steps followed:**

  ```bash
  # To embed secret.txt into image.jpg
  steghide embed -cf image.jpg -ef secret.txt

  # To extract the hidden file from image.jpg
  steghide extract -sf image.jpg
  ```
* Steghide uses a passphrase for both embedding and extraction for added security.

#### 4. 🕵️‍♂️ Security Through Obscurity:

* The practice of hiding security flaws or data by making them non-obvious.
* Learned why relying solely on obscurity is **not** a reliable security strategy.
* True security should be based on robust mechanisms, not hidden tricks.

---

### 🧠 Key Learnings:

* Basic cryptographic methods are commonly used in CTF challenges.
* CyberChef simplifies decoding encrypted data with a user-friendly interface.
* Steganography allows covert communication via media files.
* Spectrograms provide a unique method to hide/reveal data in audio formats.
* Security through obscurity should **not** be a primary method for securing systems.

---

[⬅️ Back to Day 12](Day12.md) | [➡️ Go to Day 14](Day14.md)
