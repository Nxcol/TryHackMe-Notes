# TryHackMe-Notes
Summaries of labs/rooms I've completed in cybersecurity.  
This repo serves as a **portfolio** to show my hands-on skills.# DIRB - Web Content Scanner

DIRB is a web content scanner that brute-forces hidden files and directories on a website.  
I practiced it in a lab environment (TryHackMe).

---

## 🔧 Example Commands

```bash
# Basic scan
dirb http://example.com

# With custom wordlist
dirb http://example.com /usr/share/wordlists/common.txt
