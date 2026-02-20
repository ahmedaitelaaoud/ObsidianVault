# 🛡️ Cyber Security Learning Tracker

> From fundamentals to OSCP-level penetration testing

---

## 🎯 Overall Progress

**Start Date:** {{date:YYYY-MM-DD}}
**Target Completion:** {{date+12M:YYYY-MM-DD}}
**Current Phase:** Foundation

**Overall Completion:** ████░░░░░░░░░░░░░░░░ 0%

---

## 📊 Skill Categories Overview

| Category | Progress | Status | Priority |
|----------|----------|--------|----------|
| IT Fundamentals | 0% | 🔴 Not Started | 🔥 High |
| Operating Systems | 0% | 🔴 Not Started | 🔥 High |
| Networking | 0% | 🔴 Not Started | 🔥 High |
| Security Concepts | 0% | 🔴 Not Started | 🔥 High |
| Security Tools | 0% | 🔴 Not Started | ⭐ Medium |
| Web Security | 0% | 🔴 Not Started | ⭐ Medium |
| Cryptography | 0% | 🔴 Not Started | ⭐ Medium |
| Cloud Security | 0% | 🔴 Not Started | 💤 Low |
| Forensics | 0% | 🔴 Not Started | 💤 Low |

---

## 📚 PHASE 1: IT FUNDAMENTALS

### Computer Hardware Components ⚙️
- [ ] Understand CPU, RAM, Storage (HDD vs SSD)
- [ ] Motherboard components
- [ ] Power supply basics
- [ ] Peripheral devices
- [ ] Hardware troubleshooting basics

**Resources:**
- CompTIA A+ basics
- Professor Messer videos

**Status:** ⬜ Not Started | ⏸️ In Progress | ✅ Complete

---

### Connection Types & Functions 🔌
- [ ] USB (2.0, 3.0, 3.1, Type-C)
- [ ] HDMI, DisplayPort, VGA
- [ ] Ethernet (RJ45)
- [ ] Wireless standards
- [ ] Bluetooth, NFC, Infrared

**Practical:** Connect and identify 5+ different cables

---

### Popular Software Suites 💻
- [ ] Microsoft Office Suite (Word, Excel, PowerPoint)
- [ ] Google Workspace (Docs, Sheets, Gmail)
- [ ] iCloud basics
- [ ] Cloud storage (Dropbox, OneDrive)

**Goal:** Comfortable using all major productivity suites

---

## 🐧 OPERATING SYSTEMS

### Linux Mastery 🐧
**Priority:** 🔥 CRITICAL - Most important OS for cyber security

#### Installation & Configuration
- [ ] Install Kali Linux in VirtualBox/VMware
- [ ] Install Ubuntu/Debian
- [ ] Install ParrotOS
- [ ] Dual boot setup (optional)
- [ ] VM snapshot management

#### CLI Mastery (ESSENTIAL)
Basic Commands:
- [ ] Navigation: `cd`, `ls`, `pwd`, `mkdir`, `rm`, `mv`, `cp`
- [ ] File viewing: `cat`, `less`, `more`, `head`, `tail`
- [ ] Text processing: `grep`, `sed`, `awk`, `cut`, `sort`
- [ ] Permissions: `chmod`, `chown`, `chgrp`
- [ ] Users: `useradd`, `usermod`, `passwd`, `su`, `sudo`
- [ ] Processes: `ps`, `top`, `htop`, `kill`, `killall`
- [ ] Networking: `ifconfig`, `ip`, `netstat`, `ss`
- [ ] Package management: `apt`, `apt-get`, `dpkg` (Debian)
- [ ] Archives: `tar`, `gzip`, `zip`, `unzip`
- [ ] System: `systemctl`, `service`, `journalctl`

Advanced Commands:
- [ ] `find` - locate files
- [ ] `locate` - fast file search
- [ ] `which` - command location
- [ ] `cron` - job scheduling
- [ ] `bash scripting` basics
- [ ] Pipe `|` and redirection `>`, `>>`

**Challenge:** Complete "Over The Wire: Bandit" (all 34 levels)
**Status:** Level ___ / 34

#### File System & Permissions
- [ ] Understand `/` (root), `/home`, `/etc`, `/var`, `/tmp`
- [ ] Read/Write/Execute permissions (rwx)
- [ ] Numeric permissions (chmod 755, 644, etc.)
- [ ] Special permissions (setuid, setgid, sticky bit)
- [ ] `umask` understanding

**Practice:** Create users, set permissions, test access

---

### Windows 🪟
**Priority:** ⭐ Important for enterprise environments

#### Basics
- [ ] Windows 10/11 installation
- [ ] Control Panel vs Settings
- [ ] File Explorer mastery
- [ ] User Account Control (UAC)
- [ ] Windows Defender

#### Command Line
CMD Commands:
- [ ] `dir`, `cd`, `mkdir`, `del`, `copy`, `move`
- [ ] `ipconfig`, `ping`, `tracert`, `netstat`
- [ ] `tasklist`, `taskkill`
- [ ] `net` commands (user, share, etc.)

PowerShell (More Important):
- [ ] PowerShell basics vs CMD
- [ ] Cmdlets (`Get-Process`, `Get-Service`, etc.)
- [ ] Piping in PowerShell
- [ ] Basic scripts
- [ ] Execution policy

**Goal:** Comfortable troubleshooting Windows systems

---

## 🌐 NETWORKING KNOWLEDGE

### OSI Model 📡
**Priority:** 🔥 CRITICAL - Foundation of networking

- [ ] **Layer 1 - Physical:** Cables, hubs, signals
- [ ] **Layer 2 - Data Link:** MAC addresses, switches, ARP
- [ ] **Layer 3 - Network:** IP addresses, routers, ICMP
- [ ] **Layer 4 - Transport:** TCP, UDP, ports
- [ ] **Layer 5 - Session:** Sessions, authentication
- [ ] **Layer 6 - Presentation:** Encryption, encoding
- [ ] **Layer 7 - Application:** HTTP, FTP, DNS, etc.

**Practice:** Explain each layer in own words, give examples

---

### Common Protocols & Ports 🔌
**Must Memorize:**

| Port | Protocol | Purpose | Secure Version |
|------|----------|---------|----------------|
| 20/21 | FTP | File transfer | SFTP (22) |
| 22 | SSH | Secure shell | - |
| 23 | Telnet | Remote access | SSH (22) |
| 25 | SMTP | Email sending | SMTPS (465/587) |
| 53 | DNS | Domain resolution | DNSSEC |
| 80 | HTTP | Web traffic | HTTPS (443) |
| 110 | POP3 | Email retrieval | POP3S (995) |
| 143 | IMAP | Email access | IMAPS (993) |
| 443 | HTTPS | Secure web | - |
| 3306 | MySQL | Database | - |
| 3389 | RDP | Remote desktop | - |
| 445 | SMB | File sharing | - |

**Challenge:** Identify ports from nmap scans without looking

- [ ] HTTP vs HTTPS differences
- [ ] SSL/TLS handshake process
- [ ] Certificate basics
- [ ] TCP 3-way handshake
- [ ] UDP vs TCP differences

---

### IP Addressing & Subnetting 🔢
**Priority:** 🔥 CRITICAL

#### IP Terminology
- [ ] **localhost:** 127.0.0.1 (loopback)
- [ ] **Private IP ranges:**
  - 10.0.0.0/8 (10.0.0.0 - 10.255.255.255)
  - 172.16.0.0/12 (172.16.0.0 - 172.31.255.255)
  - 192.168.0.0/16 (192.168.0.0 - 192.168.255.255)
- [ ] **Public IPs:** Everything else
- [ ] **CIDR notation:** /24, /16, etc.
- [ ] **Subnet mask:** 255.255.255.0, etc.
- [ ] **Default gateway:** Router IP
- [ ] **Broadcast address**

#### Subnetting Practice
- [ ] Calculate network/broadcast from IP/mask
- [ ] Determine usable hosts
- [ ] Subnet a network into smaller subnets
- [ ] CIDR to subnet mask conversion

**Tools:** Subnet calculator, practice quizzes
**Goal:** Subnet in your head (at least /24, /16, /8)

---

### Network Terminology 🗣️
- [ ] **VLAN:** Virtual LAN segmentation
- [ ] **DMZ:** Demilitarized zone (perimeter network)
- [ ] **ARP:** Address Resolution Protocol (IP→MAC)
- [ ] **DHCP:** Dynamic IP assignment
- [ ] **DNS:** Domain Name System
- [ ] **NAT:** Network Address Translation
- [ ] **VPN:** Virtual Private Network
- [ ] **Router:** Layer 3, routes between networks
- [ ] **Switch:** Layer 2, connects devices in LAN
- [ ] **MAN, LAN, WAN, WLAN:** Network sizes

**Practice:** Explain each term to someone non-technical

---

### Network Topologies 🕸️
- [ ] **Star:** All devices connect to central hub
- [ ] **Ring:** Devices in circular connection
- [ ] **Mesh:** Every device connects to every other
- [ ] **Bus:** Single cable backbone

**Know:** Advantages/disadvantages of each

---

## 🛠️ SECURITY TOOLS

### Reconnaissance & Scanning 🔍
- [ ] **nmap:** Port scanning king
  - [ ] Basic scans (`-sS`, `-sT`, `-sU`)
  - [ ] Service detection (`-sV`)
  - [ ] OS detection (`-O`)
  - [ ] Script scanning (`--script`)
  - [ ] Timing and stealth options
- [ ] **Netcat (nc):** Swiss army knife
- [ ] **Wireshark:** Packet analysis
- [ ] **tcpdump:** CLI packet capture
- [ ] **dig:** DNS queries
- [ ] **nslookup:** DNS lookup
- [ ] **whois:** Domain information
- [ ] **traceroute/tracert:** Path tracing

**Practice:** Scan your own network, capture packets

---

### Web Application Testing 🌐
- [ ] **Burp Suite:** Web proxy & scanner
  - [ ] Intercepting requests
  - [ ] Repeater
  - [ ] Intruder
  - [ ] Scanner (Pro)
- [ ] **OWASP ZAP:** Free web scanner
- [ ] **Nikto:** Web server scanner
- [ ] **Gobuster/Dirb:** Directory bruteforcing
- [ ] **SQLmap:** SQL injection automation

---

### Exploitation Frameworks 💥
- [ ] **Metasploit:** Exploitation framework
  - [ ] msfconsole basics
  - [ ] Search and use exploits
  - [ ] Payloads (reverse shells, meterpreter)
  - [ ] Post-exploitation
- [ ] **Social Engineering Toolkit (SET)**
- [ ] **BeEF:** Browser exploitation

**Warning:** Only use on authorized targets/labs!

---

### Password Attacks 🔐
- [ ] **John the Ripper:** Password cracking
- [ ] **Hashcat:** GPU password cracking
- [ ] **Hydra:** Online bruteforce
- [ ] **CrackMapExec:** Network authentication attacks
- [ ] **Responder:** LLMNR/NBT-NS poisoning

**Practice:** Crack hashes from CTFs (legally)

---

## 🎓 CTF CHALLENGES

### TryHackMe Progress 🚩
**Target:** 100+ rooms completed

**Beginner Rooms (Start Here):**
- [ ] Welcome
- [ ] Tutorial
- [ ] Linux Fundamentals 1, 2, 3
- [ ] Windows Fundamentals 1, 2, 3
- [ ] Networking Fundamentals
- [ ] How The Web Works
- [ ] Burp Suite Basics
- [ ] OWASP Top 10
- [ ] Metasploit Introduction
- [ ] Nmap

**Easy Boxes:**
- [ ] Pickle Rick
- [ ] RootMe
- [ ] Agent Sudo
- [ ] Simple CTF
- [ ] Bounty Hacker

**Rooms Completed:** ___ / 100
**Current Streak:** ___ days

---

### HackTheBox Progress 📦
**Target:** 20+ boxes pwned

**Starting Point Tier (Free):**
- [ ] Meow
- [ ] Fawn
- [ ] Dancing
- [ ] Redeemer

**Easy Retired Boxes:**
- [ ] Lame
- [ ] Legacy
- [ ] Blue
- [ ] Devel
- [ ] Optimum

**Boxes Pwned:** ___ User | ___ Root
**Rank:** Noob → Script Kiddie → Hacker → ...

---

### Other CTF Platforms
- [ ] **picoCTF:** Beginner-friendly (10+ challenges)
- [ ] **VulnHub:** Offline VMs (5+ machines)
- [ ] **SANS Holiday Hack:** Annual challenge

---

## 🎖️ CERTIFICATIONS PROGRESS

### CompTIA Security+ 🛡️
**Target Date:** {{date+6M:YYYY-MM-DD}}
**Status:** Not Started

**Domains:**
- [ ] 1.0 Attacks, Threats, and Vulnerabilities (24%)
- [ ] 2.0 Architecture and Design (21%)
- [ ] 3.0 Implementation (25%)
- [ ] 4.0 Operations and Incident Response (16%)
- [ ] 5.0 Governance, Risk, and Compliance (14%)

**Study Resources:**
- [ ] Professor Messer videos (all watched)
- [ ] CompTIA official study guide (read)
- [ ] Practice exams (80%+ score)
- [ ] Jason Dion practice tests
- [ ] Hands-on labs

**Practice Exam Scores:**
- Attempt 1: ___%
- Attempt 2: ___%
- Attempt 3: ___%
**Target:** 85%+ consistently before booking

---

### OSCP Preparation 💀
**Target Date:** {{date+18M:YYYY-MM-DD}}
**Status:** Not Started (Start after Security+)

**Prerequisites:**
- [ ] Strong Linux skills
- [ ] Python/Bash scripting
- [ ] 50+ HTB boxes pwned
- [ ] Metasploit mastery
- [ ] Manual exploitation comfortable

**PWK Course:**
- [ ] Enrolled
- [ ] PDF read
- [ ] Videos watched
- [ ] Lab time booked
- [ ] 30+ lab machines pwned

---

## 📖 SECURITY CONCEPTS

### Core Security Principles
- [ ] **CIA Triad:**
  - Confidentiality: Data privacy
  - Integrity: Data accuracy
  - Availability: Access when needed
- [ ] **AAA:**
  - Authentication: Who are you?
  - Authorization: What can you do?
  - Accounting: What did you do?
- [ ] **Defense in Depth:** Layered security
- [ ] **Least Privilege:** Minimum necessary access
- [ ] **Zero Trust:** Never trust, always verify

---

### Attack Types & Defenses 🎭

#### Social Engineering
- [ ] Phishing (email scams)
- [ ] Vishing (voice/phone scams)
- [ ] Smishing (SMS scams)
- [ ] Whaling (targeting executives)
- [ ] Pretexting (fabricated scenario)
- [ ] Baiting (malicious media)
- [ ] Tailgating (physical access)
- [ ] Shoulder surfing
- [ ] Dumpster diving

**Defense:** User awareness training, policies

#### Network Attacks
- [ ] DoS vs DDoS
- [ ] Man-in-the-Middle (MITM)
- [ ] DNS poisoning
- [ ] ARP spoofing
- [ ] Evil Twin (rogue AP)
- [ ] Deauth attack
- [ ] VLAN hopping
- [ ] Packet sniffing

**Defense:** Network segmentation, encryption, IDS/IPS

#### Web Attacks (OWASP Top 10)
- [ ] SQL Injection
- [ ] Cross-Site Scripting (XSS)
- [ ] Cross-Site Request Forgery (CSRF)
- [ ] Directory Traversal
- [ ] Command Injection
- [ ] Broken Authentication
- [ ] Sensitive Data Exposure
- [ ] XXE (XML External Entity)
- [ ] Insecure Deserialization
- [ ] Insufficient Logging

**Practice:** DVWA, WebGoat, PortSwigger Academy

---

### Malware Types 🦠
- [ ] Virus (self-replicating, needs host)
- [ ] Worm (self-replicating, standalone)
- [ ] Trojan (disguised malicious program)
- [ ] Ransomware (encrypts files for ransom)
- [ ] Spyware (collects information)
- [ ] Adware (unwanted advertisements)
- [ ] Rootkit (hides presence, maintains access)
- [ ] Keylogger (records keystrokes)
- [ ] Backdoor (unauthorized access method)
- [ ] Bot/Botnet (remote control, DDoS)

**Analysis:** Run samples in sandboxes (any.run, Joe Sandbox)

---

### Incident Response Process 🚨
**Remember:** PICERL

1. **Preparation:** Plans, tools, training
2. **Identification:** Detect and analyze incident
3. **Containment:** Limit damage (short-term & long-term)
4. **Eradication:** Remove threat completely
5. **Recovery:** Restore systems to normal
6. **Lessons Learned:** Post-incident review

**Practice:** Walkthrough incident scenarios

---

## 🔐 CRYPTOGRAPHY BASICS

### Core Concepts
- [ ] **Encryption:** Plaintext → Ciphertext
- [ ] **Decryption:** Ciphertext → Plaintext
- [ ] **Hashing:** One-way function (passwords)
  - MD5 (broken)
  - SHA-1 (broken)
  - SHA-256, SHA-512 (good)
- [ ] **Salting:** Random data added to hash
- [ ] **Symmetric encryption:** Same key encrypt/decrypt
  - AES, DES, 3DES
- [ ] **Asymmetric encryption:** Public/private key pair
  - RSA, ECC

### PKI (Public Key Infrastructure)
- [ ] Certificate Authority (CA)
- [ ] Digital certificates
- [ ] Certificate chain of trust
- [ ] Public vs Private keys use cases

**Practice:** Generate SSH keys, understand HTTPS certificates

---

## 📊 Weekly Progress Log

### Week of {{date:YYYY-MM-DD}}

**Hours Studied:** ___ hours
**Main Focus:** 

**Completed:**
- [ ] 
- [ ] 
- [ ] 

**CTF Challenges:** ___
**New Tools Learned:** 
**Concepts Mastered:** 

**Struggles:**


**Next Week Goals:**
1. 
2. 
3. 

**Resources Used:**
- 

---

## 🎯 Monthly Goals

### Month {{date:MMMM YYYY}}

**Primary Goal:** 

**Specific Targets:**
- [ ] Complete ___ TryHackMe rooms
- [ ] Pwn ___ HackTheBox machines
- [ ] Master ___ tools
- [ ] Study ___ hours
- [ ] Finish ___ course section

**Certifications:**
- [ ] Security+ progress: ____%

**Status:** On Track / Ahead / Behind

---

## 📚 Resource Library

### YouTube Channels
- NetworkChuck
- John Hammond
- IppSec
- LiveOverflow
- Null Byte
- HackerSploit
- Professor Messer

### Books
- [ ] "The Web Application Hacker's Handbook"
- [ ] "Penetration Testing" by Georgia Weidman
- [ ] "Metasploit: The Penetration Tester's Guide"
- [ ] "Black Hat Python" by Justin Seitz

### Online Platforms
- TryHackMe (beginner-friendly)
- HackTheBox (intermediate-advanced)
- PentesterLab
- PortSwigger Academy (free web security)
- Cybrary

### Communities
- Reddit: r/netsec, r/AskNetsec, r/cybersecurity
- Discord: TryHackMe, HackTheBox
- Twitter: #infosec, #cybersecurity

---

## 🏆 Achievements Unlocked

- [ ] First CTF challenge solved
- [ ] First machine pwned (TryHackMe)
- [ ] First HTB box rooted
- [ ] 10 CTF challenges
- [ ] 50 CTF challenges
- [ ] 100 CTF challenges
- [ ] Linux proficiency
- [ ] First certification (Security+)
- [ ] Python security tool built
- [ ] Bug bounty submission
- [ ] OSCP certified

---

*Last updated: {{date:YYYY-MM-DD}}*
*Next review: Every Sunday in Weekly Review*

**Remember:** 
- Practice legally only
- Document everything
- Learn from failures
- Security is a journey, not a destination
- Stay ethical! 🛡️
