# 🚨 SOC239 – Remote Code Execution Detected in Splunk Enterprise (EventID:201)

## 📌 Alert Overview
Detection of a malicious XSLT file upload targeting Splunk Enterprise, resulting in confirmed Remote Code Execution (RCE).

The attacker attempted to exploit the file upload functionality to execute arbitrary commands on the host system.

---

## 🖥 Affected Asset
- **Hostname:** Splunk Enterprise
- **Destination IP:** 172.16.20.13
- **HTTP Method:** POST
- **Upload Endpoint:** /en-US/splunkd/__upload/indexing/preview
- **Trigger File Path:** /opt/splunk/var/run/splunk/dispatch/1700556926.3/shell.xsl

---

## 🌐 Source Information
- **Source IP:** 180.101.88.240
- **Origin:** External (China)
- **Reputation:** Malicious
- **Known Activity:** Port scanning, SSH brute force, hacking attempts
- **Traffic Direction:** Internet → Company Network

---

## 🧠 Attack Classification
- **Attack Type:** Remote Code Execution (RCE)
- **Technique:** Malicious XSLT Upload
- **Execution Status:** Successful
- **Planned Activity:** No
- **Containment:** Performed
- **Escalated to Tier 2:** Yes

---

## 🔎 Indicators of Compromise (IOCs)

| Type          | Value |
|---------------|-------|
| Source IP     | 180.101.88.240 |
| File Name     | shell.xsl |
| File Path     | /opt/splunk/var/run/splunk/dispatch/.../shell.xsl |
| HTTP Method   | POST |
| Target Endpoint | /splunkd/__upload/indexing/preview |

---

## 🛡 MITRE ATT&CK Mapping

- **T1190** – Exploit Public-Facing Application
- **T1059** – Command and Scripting Interpreter
- **T1505** – Server Software Component

---

## 🎯 Analyst Verdict
Confirmed successful Remote Code Execution via malicious XSLT file upload targeting Splunk Enterprise. Host was contained immediately and escalated for deeper forensic investigation.

---

## 📖 Full Investigation Walkthrough
Read the complete technical breakdown here:

👉 [Full Blog Link Here](https://hashnode.com/@rideshcyber)

---

### 👨‍💻 SOC Analyst Portfolio Series
This repository is part of my ongoing SOC investigation documentation project, focused on real-world detection scenarios and incident response analysis.
