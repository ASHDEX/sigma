# Sigma Detection Rules Collection

This repository contains a curated set of **Sigma detection rules** designed to identify real-world adversary behavior across Windows, cloud, and enterprise environments.

Sigma is a generic signature format for detection logic that can be converted into SIEM-specific queries (such as Splunk, Elastic, Azure Sentinel, etc.). These rules are focused on practical threat detection scenarios and are built to support security teams in improving time-to-detect and time-to-respond.

---

## 🚀 What This Is

This project provides:
- **Original Sigma rules** for common and advanced attack techniques
- Detection logic mapped to the **MITRE ATT&CK Framework**
- Portable content usable in multiple detection platforms
- Clear descriptions and use-case context for each rule

These rules are designed for use by:
- Security Operations Center (SOC) analysts  
- Detection engineers  
- Threat hunters  
- Incident response teams

---

## 🧠 Why This Matters

Effective detection content:
- **Reduces dwell time** of attackers
- Helps SOC teams catch subtle attack patterns
- Improves defensive coverage against known TTPs
- Can be reused across environments and SIEM tools

This repository aims to support defenders in building more robust detection pipelines, enabling better security outcomes across organizations.

---

## 📦 Rules Included

Each rule includes:
- Rule name and description  
- Sigma detection logic  
- ATT&CK technique mapping  
- Severity and tag metadata  

Example rule categories:
- Credential access abuse  
- Lateral movement  
- PowerShell misuse  
- Suspicious process execution  
- Privilege escalation

> See the `rules/` directory for all rule files and the associated metadata.

---

## 📁 Usage

1. Clone this repository locally:  
   ```bash
   git clone https://github.com/ASHDEX/sigma.git
