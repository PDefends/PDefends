# 🧠 Splunk Log Collection & Monitoring Lab

This project simulates a basic centralized logging environment using **Splunk Enterprise** and **Universal Forwarders** across a Windows domain environment. The goal is to demonstrate the process of setting up Splunk, collecting Windows Event Logs, and building dashboards for security monitoring — a key part of Security Operations Center (SOC) workflows.

---

## 🖥️ Lab Environment

- **ACIWIN11** – Windows 11 Domain Workstation (Splunk Server)
- **ACIDM01** – Windows Server 2022 Domain Member (Forwarder)
- **ACIDC01** – Windows Server 2022 Domain Controller (Forwarder-ready)

---

## 🔧 Tasks Performed

### ✅ Splunk Enterprise Setup

- Installed Splunk Enterprise on `ACIWIN11`
- Configured it to listen on ports:
  - `9997` (for data input)
  - `8089` (management port)
- Allowed inbound traffic in Windows Firewall

### 🔁 Universal Forwarder Setup

- Installed Splunk Universal Forwarders on `ACIDM01`
- Used domain credentials for service configuration
- Selected **Application**, **Security**, and **System** logs for forwarding
- Forwarded logs to `192.168.0.3:9997`

### 📊 Dashboard & Analysis

Created custom dashboard panels in Splunk for:

- ✅ **Successful Logons** (`EventCode=4624`)
- 🛡️ **Privileged Logons** (`EventCode=4672`)

> These events help detect user login activity and elevated access in a Windows domain environment.

---

- Splunk login interface
- Port listening setup (9997, 8089)
- Event search results
- Dashboard with panels for 4624 and 4672

---

## 🎯 Purpose

This lab reinforces my ability to:

- Set up a basic **SIEM pipeline**
- Ingest Windows Event Logs from multiple endpoints
- Visualize key security events using **Splunk dashboards**

I aim to work as a **SOC Analyst**, and I'm deepening my understanding of Splunk — not just from a beginner’s perspective, but with practical, hands-on configurations. This is a checkpoint in my journey, not just the starting point.

---

## 🏷️ Tags

`#Splunk` `#SIEM` `#SOCAnalyst` `#WindowsLogs` `#EventID4624` `#EventID4672` `#CyberLab` `#InfoSec` `#HandsOnSkills`
