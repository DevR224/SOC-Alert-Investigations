# SOC138 – Detected Suspicious XLS File

## Overview
This document summarizes the key Indicators of Compromise (IOCs) and findings identified during the investigation of the **SOC138 – Detected Suspicious XLS File** alert on the LetsDefend platform.

A detailed step-by-step investigation walkthrough is documented separately on my Hashnode blog.

---

## Alert Summary
- **Alert Name:** SOC138 – Detected Suspicious XLS File
- **Affected Host:** 172.16.17.56
- **Threat Type:** Malicious XLS file
- **Host Status:** Quarantined (Contained)
- **C2 Activity:** Observed

---

## Key Findings
- The host generated **unexpected outbound network traffic**
- The XLS file and associated URL were confirmed **malicious via VirusTotal**
- Evidence of **Command-and-Control (C2) communication** was identified
- The host system was already contained at the time of investigation
- Alert reinvestigation revealed minor containment status inconsistency, likely platform-related

---

## Indicators of Compromise (IOCs)

### IP Addresses
- `177.53.143.89` – Suspicious external IP associated with C2 communication

### File Indicators
- **File Type:** XLS
- **File Hash:** (Identified during investigation and verified via VirusTotal)

### Network Indicators
- Unexpected outbound traffic from the affected host
- Suspicious external communication shortly after alert creation

---

## Analyst Verdict
The XLS file was confirmed **malicious**, and the alert represents a **true positive**.  
Containment actions were appropriate, and no further compromise was observed after isolation.

---

## Full Investigation Walkthrough
For a complete analysis walkthrough with screenshots and reasoning:

🔗 **Hashnode Blog:**  
https://soc138-detected-suspicious-xls-file.hashnode.dev/soc138-detected-suspicious-xls-file-soc-alert-walkthrough?showSharer=true

---

## About This Repository
This repository is maintained to showcase **SOC alert investigation experience**, IOC extraction, and incident response reasoning for practical SOC environments.

