# Enterprise Network Security & SOC Homelab

## 📌 Overview

This project simulates a real-world enterprise network environment with segmentation, monitoring, detection, and response capabilities. The lab was built to develop hands-on experience aligned with Network Security and Cybersecurity Analyst roles.

The environment includes firewall segmentation, SIEM monitoring, IDS/IPS detection, vulnerability scanning, and attack simulation.

---

## 🎯 Objectives

* Design a segmented network using pfSense and Cisco switches
* Monitor network and system activity using a SIEM (Splunk)
* Detect and analyze malicious activity using IDS/IPS (Suricata)
* Perform vulnerability assessments using OpenVAS
* Investigate security incidents and perform root cause analysis
* Harden systems based on identified vulnerabilities

---

## 🏗️ Lab Architecture

Internet (optional)

↓

pfSense Firewall (FW-EDGE01)

↓

├── LAN1 (Enterprise Network)

│   ├── AD-DC01 (Domain Controller)

│   ├── AD-WIN10 / AD-WIN11

│   ├── SIEM-SPLUNK01

│   └── ATTACK-KALI01

│

└── LAN2 (Vulnerable Network)

├── VULN-METASPLOITABLE2

├── VULN-DVWA / WebGoat

├── VULN-WIN2019 (Unpatched)

└── VULN-UBU-OLD

---

## 🧰 Technologies Used

### Networking & Infrastructure

* pfSense (Firewall, NAT, VLANs)
* Cisco Catalyst 3560 / 3750 (Switching, VLAN segmentation)
* Proxmox (Virtualization platform)

### Security Tools

* Splunk (SIEM & log analysis)
* Suricata (IDS/IPS)
* OpenVAS (Vulnerability scanning)
* Sysmon (Windows logging)

### Attack Simulation

* Kali Linux (Offensive testing)
* Metasploitable / DVWA (Vulnerable targets)

---

## 🔍 Key Implementations

### 1. Network Segmentation

* Created multiple LANs (Enterprise vs Vulnerable)
* Implemented VLAN-based isolation
* Controlled traffic using firewall rules

### 2. Centralized Logging (SIEM)

* Forwarded logs from pfSense, Windows, and Linux systems to Splunk
* Built dashboards for:

  * Failed login attempts
  * Network scans
  * Suspicious traffic

### 3. Intrusion Detection & Prevention

* Deployed Suricata on pfSense
* Detected:

  * Port scans
  * Brute-force attempts
  * Web attacks (SQL injection)

### 4. Incident Detection & Analysis

* Simulated attacks using Kali Linux
* Investigated alerts in Splunk
* Performed root cause analysis:

  * Identified attacker IP
  * Traced affected systems
  * Determined attack method

### 5. Vulnerability Management

* Conducted scans using OpenVAS
* Identified critical vulnerabilities (CVEs)
* Prioritized remediation based on severity

### 6. System Hardening

* Disabled insecure services (e.g., SMBv1)
* Implemented firewall restrictions
* Applied least-privilege principles
* Reduced attack surface across systems

---

## 🧪 Example Attack Scenarios

### Scenario 1: Port Scanning

* Tool: Nmap (Kali Linux)
* Detection: Suricata + pfSense logs
* Analysis: Splunk dashboard

### Scenario 2: Brute Force Login Attempt

* Tool: Hydra
* Detection: Failed login logs (Windows + Splunk)
* Response: Blocked source IP via firewall

### Scenario 3: Web Application Attack

* Target: DVWA
* Attack: SQL Injection
* Detection: Suricata alerts
* Mitigation: Rule tuning and firewall blocking

---

## 📊 Skills Demonstrated

* Network Security (VLANs, segmentation, firewall rules)
* SIEM Monitoring & Log Analysis
* Incident Response & Root Cause Analysis
* Vulnerability Management
* IDS/IPS Deployment & Tuning
* Security Hardening

---

## 🚀 Future Enhancements

* Active Directory attack simulations (Kerberos, Pass-the-Hash)
* Automated alerting and response
* Threat intelligence integration
* Cloud security integration (AWS/Azure)

---

## 📌 Conclusion

This lab demonstrates practical, hands-on experience in detecting, analyzing, and mitigating security threats within a simulated enterprise environment. It aligns closely with real-world responsibilities of Network Security and Cybersecurity Analyst roles.
