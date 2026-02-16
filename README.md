# Domain Mapper

Domain Mapper is a Bash-based framework for automated Active Directory reconnaissance and attack-chain execution. It combines scanning, enumeration, exploitation checks, and reporting into a structured workflow.

---

## Overview

Domain Mapper operates in four stages:

1. Scanning – Identifies live hosts and open ports  
2. Enumeration – Discovers infrastructure roles and Active Directory objects  
3. Exploitation – Performs vulnerability checks and credential testing  
4. Reporting – Generates structured output  

Each stage supports three levels: Basic, Intermediate, and Advanced.  
Higher levels include lower-level functionality.

---

## Capabilities

### Scanning
- Top 1000 TCP ports  
- Full TCP scan (1–65535)  
- TCP and UDP scanning (Masscan)  

### Enumeration
- Service and version detection  
- Domain Controller identification  
- DHCP, DNS, and Default Gateway discovery  
- SMB share enumeration  
- DNS brute-force checks  
- Anonymous LDAP checks  
- SMB protocol and signing analysis  
- Authenticated Active Directory enumeration:
  - Users  
  - Groups  
  - Shares  
  - Password policy  
  - Disabled accounts  
  - Non-expiring accounts  
  - Domain Admin members  

### Exploitation
- NSE vulnerability scanning (vuln, vulners)  
- Password spraying  
- Kerberos ticket extraction  
- Offline cracking with John  

---

## Requirements

Tested on Kali Linux.

Required tools:

- nmap  
- masscan  
- netexec / crackmapexec  
- impacket  
- john  
- figlet  

## Installation

Clone the repository:

```bash
git clone https://github.com/mishap2001/domain-mapper.git
cd domain-mapper
```

Install dependencies:

```bash
sudo apt update
sudo apt install nmap masscan netexec crackmapexec john figlet
```

Make the script executable:

```bash
chmod +x domain-mapper.sh
```

## Usage

Run as root:

```bash
sudo ./domain-mapper.sh
```

If the file name contains a space:

```bash
sudo bash Domain\ Mapper.sh
```


```bash
sudo apt update
sudo apt install nmap masscan netexec crackmapexec john figlet
```

## Usage

If the file name contains a space:

```bash
sudo bash Domain\ Mapper.sh
```

Alternatively, rename the file to avoid spaces:

```bash
sudo bash domain-mapper.sh
```

