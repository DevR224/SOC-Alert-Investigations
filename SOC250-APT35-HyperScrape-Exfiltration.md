# 🚨 SOC250 – APT35 HyperScrape Data Exfiltration Tool Detected (EventID:212)

## 📌 Incident Summary

This repository documents a Security Operations Center (SOC) investigation involving activity associated with APT35 and the HyperScrape data exfiltration tool.

The alert revealed suspicious Exchange mailbox access, unauthorized email harvesting, and communication with malicious external infrastructure.

---

## 🧠 Threat Overview

- **Threat Actor:** APT35  
- **Tool Identified:** HyperScrape  
- **Attack Type:** Data Exfiltration  
- **Target:** Email Infrastructure  
- **Severity:** High  

---

## 🔍 Key Investigation Findings

- Suspicious Exchange log activity indicating mailbox scraping  
- Execution of `EmailDownloader.exe` process  
- Scheduled task activity suggesting persistence  
- Communication with previously reported malicious IP (136.243.108.14)  
- Confirmed external threat infrastructure  

---

## 🛡 MITRE ATT&CK Techniques Observed

- T1114 – Email Collection  
- T1059 – Command and Scripting Interpreter  
- T1071 – Application Layer Protocol  
- T1589 – Gather Victim Identity Information  

---

## 🎯 Incident Response Actions

- Host log correlation and SIEM analysis  
- IP reputation validation  
- Endpoint process review  
- Scope assessment  
- Immediate host containment  

---

## 📊 Outcome

The investigation confirmed a true positive involving unauthorized mailbox access and data harvesting consistent with APT-style reconnaissance and exfiltration.

The affected host was successfully contained to prevent further impact.

---

## 📖 Full Technical Walkthrough

Read the complete step-by-step investigation, log analysis, and containment decision-making process here:

👉 **[FULL BLOG LINK HERE](https://hashnode.com/@rideshcyber)**

---

## 👨‍💻 About This Repository

This repository is part of my SOC Analyst portfolio series, demonstrating practical incident response, threat intelligence validation, and advanced persistent threat investigation techniques.
