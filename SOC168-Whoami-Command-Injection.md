# 🚨 SOC168 – Whoami Command Detected in Request Body(EventID:118)

## 📌 Alert Overview
Detection of `whoami` command inside an HTTP POST request body targeting an internal web server.

This activity indicates a potential **Command Injection attack** attempt.

---

## 🖥 Affected Asset
- **Hostname:** WebServer1004
- **Destination IP:** 172.16.17.16
- **Requested Endpoint:** /video/
- **HTTP Method:** POST

---

## 🌐 Source Information
- **Source IP:** 61.177.172.87
- **Reputation:** Malicious
- **Known For:** SSH attacks, brute-force activity
- **Traffic Direction:** Internet → Company Network

---

## 🧠 Attack Classification
- **Attack Type:** Command Injection
- **Command Observed:** whoami
- **Execution Status:** Successful
- **Planned Activity:** No
- **Containment Required:** Yes
- **Escalated to Tier 2:** Yes

---

## 🔎 Indicators of Compromise (IOCs)

| Type        | Value              |
|-------------|--------------------|
| Source IP   | 61.177.172.87      |
| Command     | whoami             |
| HTTP Method | POST               |
| Target URL  | /video/            |

---

## 🎯 Analyst Verdict
Confirmed successful command injection attempt from external malicious IP. Host was contained and escalated for further investigation.

---

## 🛡 MITRE ATT&CK Mapping
- **T1059** – Command and Scripting Interpreter
- **T1190** – Exploit Public-Facing Application

---

## 📖 Full Investigation Walkthrough
Read the complete step-by-step SOC analysis here:

👉 [Full Blog Link Here](https://rideshcyber.hashnode.dev/soc168-whoami-command-detected-in-request-body-walkthrough-eventid-118)

---

### 👨‍💻 SOC Analyst Portfolio Series
This repository is part of my ongoing SOC investigation documentation series based on real-world detection scenarios.
