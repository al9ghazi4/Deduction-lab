# Cybersecurity Monitoring & Detection Lab

This GitHub repository documents a comprehensive cybersecurity lab environment for monitoring, detection, and attack simulation. The lab integrates tools such as pfSense, Security Onion, Splunk, Active Directory, and vulnerable machines to create a hands-on learning platform for cybersecurity analysis and incident response.

## 🎯 Objective
The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

## 🧠 Skills Learned
- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

## 🛠 Tools Used
- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## 📋 Lab Overview
**Host Machine Specs:**
- OS: Windows 11 Pro for Workstations   
- Virtualization: VMware Workstation Pro

**Virtual Machines Used:**
- pfSense Firewall
- Windows 11 (PC1)
- Windows Server 2019 (Domain Controller)
- Kali Linux (Attacker)
- Metasploitable 2 (Victim)
- Security Onion (IDS/Monitoring)
- Splunk Server (SIEM)

**Network Segments:**
- WAN: 192.168.114.0/24
- LAN: 192.168.1.0/24
- Attacker: 192.168.3.0/24
- Security Onion: 192.168.4.0/24
- Splunk: 192.168.5.0/24

## 🌐 Network Topology
A detailed diagram showing VMNet mappings and subnet roles is available in  https://github.com/al9ghazi4/Deduction-lab/commit/dfbdc576d633c3bee04a685ed8576bc9c72cbb8b

## 🔐 pfSense Setup
- Installed pfSense 2.6.0 and mapped interfaces.
- Assigned static IPs per segment (LAN, SPAN, KALI, SECONION, SPLUNK).
- Enabled DHCP and bridged LAN with SPAN.
- Applied firewall rules to allow traffic for all interfaces.

## 🧠 Active Directory Configuration
- Installed Windows Server 2019 and configured as a Domain Controller.
- Created domain `test.local` with DNS and Reverse Lookup Zones.
- Deployed a vulnerable AD script for testing attacks.
- Joined Windows 11 to domain and created users/groups.

## 🐧 Kali Linux & Metasploitable Setup
- Deployed Kali Linux for attack simulation.
- Metasploitable 2 VM used as a vulnerable target.
- Attacks launched using tools like `nmap`, `msfconsole`, and `kerbrute`.

## 🧅 Security Onion Installation & Alerts
- Security Onion 2.3 installed with management and monitoring interfaces.
- SOC dashboards configured for Alerts, Hunt, Dashboards, Cases, PCAP.
- Detected real-time attacks such as scanning and Kerberoasting.

## 📈 Splunk Deployment & Monitoring
- Installed Splunk 9 on both Linux and Windows.
- Configured receiver (port 9997) and created custom index.
- Deployed forwarder on Windows Server to ingest event logs.
- Correlated events in Splunk UI and created dashboards.

## ⚠️ Attack Detection Workflow
**Scenario 1:**
- Source: Kali Linux (192.168.3.2)
- Target: Windows Server 2019 (192.168.1.100)
- Attack: Port scan & Kerberoasting
- Detection: Security Onion alerts + Splunk log correlation

## 📂 screenshots
  - 

