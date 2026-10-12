# 🚩 CTF Writeups & Security Challenges

Welcome! This repository contains writeups, walkthroughs, and problem-solving methodologies for Capture The Flag (CTF) competitions, platform challenges, and practical cybersecurity tasks.

The main goal of this repository is to document my analytical workflow, share problem-solving techniques, and demonstrate practical exploitation and analysis skills across various domains.

---

## 🎯 Main CTF Categories & Focus Areas

* **Digital Forensics & Incident Response (DFIR):**
  * Memory analysis (RAM dumps via Volatility).
  * Network traffic inspection and packet analysis (Wireshark, PCAP files).
  * File carving, disk image analysis, and recovering hidden or deleted artifacts.

* **Web Application Security:**
  * Identifying and exploiting vulnerabilities (SQL Injection, XSS, SSRF, IDOR, RCE).
  * Authentication and session management bypasses.
  * Analyzing business logic flaws and API security issues.

* **Cryptography & Encoding:**
  * Breaking classical ciphers and weak encryption implementations.
  * RSA analysis (weak keys, common modulus attacks using RsaCtfTool).
  * Hash identification and cracking (Hashcat, John the Ripper).

* **Reverse Engineering & Binary Analysis:**
  * Static and dynamic analysis of compiled binaries (ELF, PE).
  * Using disassemblers and decompilers (Ghidra, IDA Free).
  * Identifying logic flaws, hardcoded credentials, and patching binaries.

* **OSINT & Miscellaneous (Steganography / Encoding):**
  * Uncovering hidden data in images, audio, and text files (Steghide, ExifTool).
  * Data decoding, data manipulation, and custom script automation (Python).

---

## 🛠️ CTF Toolkit

| Category | Tools & Frameworks |
| :--- | :--- |
| **Web Exploitation** | Burp Suite, ffuf, Gobuster, SQLmap, Postman, Caido |
| **Forensics & Analysis** | Wireshark, Volatility 3, CyberChef, Binwalk, ExifTool, Autopsy |
| **Reverse Engineering & Pwn** | Ghidra, IDA Pro/Free, GDB (Pwndbg/GEF), Rizin, Checksec |
| **Crypto & Decoding** | CyberChef, RsaCtfTool, Hashcat, John the Ripper, Python (pwntools) |
| **Automation & Scripting** | Python 3 (Requests, Pwntools, Beautiful Soup), Bash scripting |

---

## 💡 Writeup Methodology & Structure

Every writeup in this repository follows a consistent, analytical format:

1. **Challenge Overview:** Platform name, category, difficulty rating, and initial challenge description.
2. **Reconnaissance & Analysis:** How the target was examined, what clues were found, and initial vulnerability assessment.
3. **Exploitation / Step-by-Step Walkthrough:** Detailed reproduction of the attack path, commands executed, or scripts written.
4. **Rabbit Holes & Missteps:** Documenting failed attempts or incorrect hypotheses to highlight troubleshooting and critical thinking.
5. **Flag Extraction:** How the final flag was successfully retrieved and validated.

---

## ⚠️ Legal & Ethical Disclaimer

All writeups, solutions, and scripts in this repository were created and published **strictly for educational, training, and defensive purposes** as part of legal CTF competitions (TryHackMe, HackTheBox, PicoCTF, etc.) or authorized security platforms.

* Solutions to active competitions or active boxes are handled responsibly according to platform rules.
* No techniques from this repository are intended for unauthorized access, malicious hacking, or illegal activities.
