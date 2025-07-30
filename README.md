# SOC-Analyst-Lab-Project
SOC Analyst Simulation Project: Attack Detection Using Splunk

🛡️ Project Overview

This project simulates real-world cyberattacks on a vulnerable machine and demonstrates how a SOC Analyst would detect and investigate these attacks using Splunk, a Security Information and Event Management (SIEM) tool.

The project focuses on:

Network reconnaissance (via Nmap)

Brute-force attacks (via FTP login attempts)

Potential backdoor exploitation

All attacks are simulated in a controlled lab environment using virtual machines.

🧰 Tools & Technologies Used

Splunk (installed on Ubuntu VM)

Metasploitable 2 (as the vulnerable target)

Kali Linux (as the attacker machine)

VirtualBox (to run VMs)

Nmap (for scanning)

Hydra or ftp brute-force (for credential attacks)

🧪 Attack Simulation Steps

1. 🔍 Nmap Scan

Objective: Identify open ports on the Metasploitable machine.

Command used:

nmap -sS -sV -T4 192.168.56.105

Logs generated: Detected by Splunk as port scan activity.

2. 🔐 FTP Brute-force

Objective: Attempt to gain access via FTP.

Tool used: ftp or hydra

Target: Port 21 (vsFTPd 2.3.4)

Credential used: msfadmin / msfadmin

Logs generated: Multiple login attempts flagged in Splunk.

3. 🦠 (Optional) Backdoor / Exploit

Objective: Exploit known vulnerability (if applicable)

Example: Backdoor in vsFTPd 2.3.4 or a meterpreter shell via Metasploit

🔎 Detection in Splunk

After simulating the attacks, Splunk is used to:

Search logs for suspicious activity

Detect brute-force attempts through login failure patterns

Monitor FTP access and connections

Create dashboards and alerts

Example Search Queries:

index=main sourcetype=vsftpd.log "Failed login"
index=main sourcetype=syslog "Nmap scan detected"

📷 Screenshots



(You can update this section as you progress)

🧠 Learning Outcomes

Hands-on experience with real attack vectors

SIEM setup and log analysis using Splunk

Understanding of network behavior under attack

Basic incident detection and investigation skills

📁 Project Structure

SOC-Detection-Project/
├── screenshots/
│   ├── ftp_connection.png
│   ├── ftp_listing.png
│   └── splunk_dashboard.png
├── README.md
├── attack-scripts/
│   └── brute_force.sh
└── queries/
    └── splunk_searches.txt

🚀 Future Work

Add backdoor exploit detection

Integrate with Suricata or Zeek for deeper network inspection

Automate alerts in Splunk
