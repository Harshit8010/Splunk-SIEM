# 📊 Splunk SIEM

A virtual lab project built to demonstrate centralized security monitoring using **Splunk Enterprise** as a SIEM. This project collects and analyzes logs from various sources including a Cowrie SSH honeypot, Wazuh HIDS agents, OPNsense firewall, and Windows Sysmon. It simulates attacker behavior and enables real-time alerting and log correlation across systems—ideal for SOC analysis and threat hunting.

---

## 🎯 Project Objectives

✅ Deploy and configure Splunk on Kali Linux  
✅ Ingest logs from multiple systems (Wazuh, Cowrie, OPNsense, Sysmon)  
✅ Detect threats like brute-force, port scans, and reverse shells  
✅ Build dashboards and alerts using SPL queries  
✅ Correlate logs across honeypot, firewall, and endpoint sources  
✅ Document attack simulation and response workflows  

---

## ⚙️ Lab Overview

| Component         | Role                                |
|------------------|-------------------------------------|
| Kali Linux        | Splunk Server + Cowrie Honeypot     |
| CSI Linux         | Wazuh Manager (Linux Agent)         |
| Windows Server    | Wazuh Agent + Sysmon Logs           |
| OPNsense Firewall | Log Source via Syslog               |

---

## 🔌 Integrated Log Sources

- 🛡️ **Wazuh** – HIDS alerts, Sysmon (Windows)
- 🐍 **Cowrie** – SSH honeypot logs via HEC
- 🌐 **OPNsense** – Syslogs via UDP (port 514)
- 🐧 **Journald** – Local Linux logs (auth, ssh, cron)

---

## 📦 Project Structure

Splunk-SIEM-Project/

├──  README.md # Project overview

├──  setup.md # Splunk installation & configuration

├── log-sources-setup/        

│   ├── HIDS_splunk_forwader.md

│   ├── Honeypot_splunk_integration.md

│   ├── local_linux_splunk_integration.md

│   ├── router&firewall_splunk_forwarding.md

│   └── windows_test-data_ingestion.md

├── report.md # Attack simulation, SPL queries, analysis

└── screenshots/ # Visual logs, dashboard samples

---

## 🛠️ Tools & Technologies

- **Splunk Enterprise** – SIEM platform  
- **Wazuh HIDS** – Host-based intrusion detection  
- **Cowrie Honeypot** – SSH honeypot logs  
- **OPNsense** – Firewall syslog forwarding  
- **Sysmon + Universal Forwarder** – Windows endpoint logs  
- **SPL (Search Processing Language)** – Log analysis  

---

## 📈 Why This Project Matters

This lab simulates realistic attacks and demonstrates how Splunk can:

- Centralize and correlate logs from varied sources  
- Detect known attack techniques like brute-force or reverse shells  
- Generate real-time alerts and create visual dashboards  
- Help analysts track attacker movement across a network  

---

## 📚 References

- [Splunk Docs](https://docs.splunk.com)
- [Wazuh Docs](https://documentation.wazuh.com)
- [Cowrie Honeypot](https://github.com/cowrie/cowrie)
- [OPNsense](https://docs.opnsense.org/)

---
