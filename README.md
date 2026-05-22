# Sigma Detection Rules

Custom Sigma detection rules for identifying adversary behavior across Windows, cloud, and enterprise environments. Rules are SIEM-portable and mapped to the MITRE ATT&CK framework.

## Overview

Sigma is an open, vendor-agnostic signature format for SIEM detection logic. Rules in this repository can be converted to platform-specific queries for Splunk, Microsoft Sentinel, Elastic SIEM, QRadar, and other compatible platforms using tools such as `sigmac` or `pySigma`.

## Rule Categories

| Category | Description |
|---|---|
| Credential Access | AS-REP Roasting, Kerberoasting, LSASS dumps, Pass the Hash |
| Lateral Movement | PsExec, WMI execution, SMB-based propagation |
| Privilege Escalation | Token impersonation, UAC bypass, service abuse |
| Persistence | Registry run keys, scheduled tasks, startup folders |
| Defense Evasion | PowerShell obfuscation, LOLBAS abuse, log clearing |
| C2 & Exfiltration | Suspicious outbound connections, DNS tunneling |
| Discovery | Network scanning, AD enumeration, account discovery |

## Rule Structure

Each rule follows the Sigma specification and includes:

- `title` — human-readable rule name
- `description` — detection context and adversary behavior
- `logsource` — target log category and product
- `detection` — condition logic with selection filters
- `tags` — MITRE ATT&CK technique IDs (e.g., T1003, T1059)
- `level` — severity (informational, low, medium, high, critical)
- `falsepositives` — known benign activity that may trigger the rule

## Usage

Convert rules to SIEM-specific queries using pySigma:

```bash
# Install pySigma
pip install pySigma

# Convert to Splunk SPL
sigma convert -t splunk rules/credential_access/lsass_dump.yml

# Convert to KQL (Microsoft Sentinel)
sigma convert -t microsoft365defender rules/lateral_movement/psexec_execution.yml
```

## Compatibility

Tested against the following platforms:

- Microsoft Sentinel (KQL)
- Splunk Enterprise Security (SPL)
- Elastic SIEM (EQL / Lucene)
- IBM QRadar (AQL)

## Author

ASHDEX — Security Researcher & Architect | Detection Engineering
[ashdex.com](https://ashdex.com)
