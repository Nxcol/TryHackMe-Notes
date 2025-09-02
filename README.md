# TryHackMe-Notes
Summaries of labs/rooms I've completed in cybersecurity.  
This repo serves as a **portfolio** to show my hands-on skills.

# DIRB - Web Content Scanner

DIRB is a web content scanner that brute-forces hidden files and directories on a website.  
I practiced it in a lab environment (TryHackMe).

---

## 🔧 Example Commands

```bash
# Basic scan
dirb http://example.com

# With custom wordlist
dirb http://example.com /usr/share/wordlists/common.txt 
```

# Shodan Practice Report – Apache Servers in US

## 🎯 Task
Search for Apache servers in the United States using Shodan.  
Identify exposed versions, note potential risks, and provide recommendations.  

```## 🔍 Findings
1. **Apache 2.4.6 (CentOS)**
   - Host: demosmoscareoptimized.com (AWS, US)
   - Risk: Very outdated (released 2013). Contains many known vulnerabilities (DoS, privilege escalation, etc.).

2. **Apache 2.4.58 (Ubuntu)**
   - Host: helpdesk.ptdata.co.uk (DigitalOcean, UK)
   - Risk: Recent version (released 2023). Lower risk, but still requires ongoing patching.

## ⚠️ Risks
- Apache 2.4.6 has numerous CVEs, making it an easy target if unpatched.
- Outdated services exposed on the internet increase the attack surface.

## ✅ Recommendations
- Upgrade Apache 2.4.6 to the latest supported release.
- Regularly patch and update web servers.
- Limit public exposure of services to only what’s necessary.
- Monitor access logs for suspicious activity.

## 📝 Notes
- Data gathered only via Shodan’s search engine (no interaction with systems).
- Purpose: Learning and practicing asset discovery and vulnerability assessment.
```

## 🦠 Virus Total ##

## 📖 What is it?
VirusTotal is a free tool to check files, URLs, and IPs against multiple antivirus engines.  
It’s used in cybersecurity to quickly spot malware or phishing.  

---

## 🛠️ Example Use / Scenario
**Scenario:**  
- A user receives an email with a suspicious attachment: `invoice2025.exe`.  

**Steps I Took:**  
1. Saved the file safely (without opening it).  
2. Uploaded it to [VirusTotal](https://www.virustotal.com).  
3. Reviewed results across 60+ antivirus engines.  
4. Saw several flagged it as malicious.  
5. Decided actions: block sender, warn user, update incident report.  

---

## ✅ Skills Learned
- How to safely check files/links without risk.  
- Reading and interpreting VirusTotal reports.  
- Applying results in a SOC-style workflow (incident response).  
