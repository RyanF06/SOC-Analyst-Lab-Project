# 🛡️ SOC Analyst Lab Project: Detecting Cyber Attacks Using Splunk SIEM

## 📌 Overview

This project simulates real-world cyberattacks in a controlled lab and shows how to detect them using Splunk SIEM.

## 🧰 Lab Environment

| Role         | Machine           | OS                              |
|--------------|-------------------|----------------------------------|
| Attacker     | Kali Linux        | Kali Rolling                     |
| Victim       | Metasploitable 2  | Linux (intentionally vulnerable) |
| SIEM Server  | Ubuntu            | Ubuntu 20.04 with Splunk         |

- **Network**: Host-only or Internal NAT
- **Logging**: Forward system logs to Splunk (syslog or universal forwarder)
- **Splunk Access**: Browser (default port 8000)

## 📂 Modules

- [Nmap Port Scanning Detection](./README_NMAP.md)
- [SSH Brute-force Detection](./README_BRUTEFORCE.md)
- [Reverse Shell Detection](./README_SHELL.md)
- [Splunk Dashboards & Alerts](./README_SPLUNK.md)

# 🔍 Nmap Port Scan Detection

## Objective

Simulate a typical reconnaissance scan and detect it in Splunk.

## Tool

- `nmap`

## Attack Command

```bash
nmap -sS -T4 -p- 192.168.1.46
