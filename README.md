# OWASP-BWA-VAPT-Project
Vulnerability Assessment and Penetration Testing of OWASP Broken Web Applications using Kali Linux.

## Project Overview

This project demonstrates a complete Vulnerability Assessment and Penetration Testing (VAPT) engagement against the OWASP Broken Web Applications (OWASP BWA) virtual machine using Kali Linux.

The assessment was conducted in a controlled lab environment for educational and research purposes.

## Lab Setup

### Attacker Machine

- Kali Linux
- IP Address: 10.0.2.4

### Target Machine

- OWASP Broken Web Applications
- IP Address: 10.0.2.3

---

## Objectives

- Host Discovery
- Network Enumeration
- Service Enumeration
- Technology Fingerprinting
- Directory Enumeration
- Authentication Testing
- Vulnerability Scanning
- Security Assessment

---

## Tools Used

| Tool | Purpose |
|--------|---------|
| arp-scan | Host Discovery |
| ping | Connectivity Testing |
| Nmap | Port Scanning |
| WhatWeb | Technology Fingerprinting |
| Gobuster | Directory Enumeration |
| Hydra | Password Auditing |
| DVWA | Vulnerability Testing |
| OpenVAS | Vulnerability Assessment |

---

## Methodology

### 1. Host Discovery

```bash
arp-scan -l
```

### 2. Connectivity Testing

```bash
ping 10.0.2.3
```

### 3. Port Enumeration

```bash
nmap -sV -sT -p- 10.0.2.3
```

### 4. Technology Detection

```bash
whatweb -v http://10.0.2.3
```

### 5. Directory Enumeration

```bash
gobuster dir -u http://10.0.2.3 -w wordlist.txt
```

### 6. Authentication Testing

```bash
hydra -l admin -P rockyou.txt 10.0.2.3 http-post-form
```

### 7. Vulnerability Assessment

Performed using OpenVAS.

---

## Key Findings

- Weak credentials identified
- Multiple open services
- Legacy software versions
- Exposed administrative interfaces
- Critical OpenVAS findings

---

## Screenshots

See screenshots folder.

---

## Disclaimer

This project was performed within an isolated lab environment for educational purposes only.

