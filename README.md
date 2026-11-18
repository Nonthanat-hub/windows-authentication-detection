
# Windows Authentication Log Analysis & Brute Force Detection

A Python-based Security Operations Center (SOC) portfolio project focused on analyzing Windows Security Event Logs and detecting suspicious authentication activities.

## Project Overview

This project aims to analyze Windows authentication events, identify suspicious login patterns, and generate security alerts using Python.

The project simulates a Tier 1 SOC Analyst workflow, from log collection and data processing to threat detection and incident reporting.

## Objectives

- Analyze Windows Security Event Logs.
- Identify failed and successful login activities.
- Detect potential brute-force attacks.
- Identify suspicious authentication patterns.
- Generate structured security alerts.
- Map relevant findings to MITRE ATT&CK.

## Detection Scope

| Event ID | Description |
|---|---|
| 4624 | Successful logon |
| 4625 | Failed logon |
| 4740 | User account locked out |

## Technologies

- Python
- Pandas
- Jupyter Notebook
- Windows Security Event Logs
- Git & GitHub
- MITRE ATT&CK

## Project Structure

```text
windows-authentication-detection/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── src/
├── reports/
├── docs/
├── tests/
├── images/
└── README.md
```

## Planned Workflow

1. Collect Windows authentication logs.
2. Parse and clean log data.
3. Analyze login activity.
4. Develop brute-force detection rules.
5. Investigate suspicious events.
6. Generate SOC-style incident reports.

## Project Status

**Status:** In Progress

This repository is being developed as a hands-on SOC Analyst portfolio project.

## Disclaimer

This project is intended for educational and defensive cybersecurity purposes only. Testing will be performed using authorized lab environments and security event datasets.
