# SOC169 – Possible IDOR Attack Detected (EventID:119)

This file contains the Indicators of Compromise (IOCs) and technical highlights from the SOC169 alert investigation involving a successful IDOR (Insecure Direct Object Reference) attack.

📖 For the complete step-by-step investigation, analysis reasoning, containment process, and lessons learned, read the full blog here:  
👉 [Read Full Walkthrough on Hashnode](https://rideshcyber.hashnode.dev/soc169-possible-idor-attack-detected-walkthrough-eventid-119)

---

## 📌 Alert Overview

- **Event ID:** 119  
- **Hostname:** WebServer1005  
- **Destination IP:** 172.16.17.15  
- **Source IP:** 134.209.118.137  
- **Network Direction:** Internet → Company Network  
- **HTTP Method:** POST  
- **Endpoint Targeted:** `/get_user_info/`  
- **Trigger Reason:** Consecutive requests to same page  

---

## 🚩 Indicators of Compromise (IOCs)

### 🔹 Suspicious Source IP
134.209.118.137

- External network origin  
- Previously reported for brute-force and SSH-related malicious activity  

---

### 🔹 Targeted Endpoint
https://172.16.17.15/get_user_info/

- Sensitive endpoint exposing user information  
- Repeated POST requests observed  
- Parameter manipulation attempts detected  

---

### 🔹 User-Agent String
Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.1.4322)


- Outdated browser signature  
- Commonly used in scripted or automated attacks  

---

## 🎯 Attack Classification

- **Attack Type:** IDOR (Insecure Direct Object Reference)  
- **Attack Success:** Yes  
- **Data Accessed:** Unauthorized user information  
- **Containment Action:** Host isolated  
- **Escalation:** Tier 2 Analyst  

---

## 🛡 Why This Matters

IDOR vulnerabilities exploit improper access control logic rather than software bugs.  
Attackers can retrieve sensitive data simply by manipulating request parameters.

This case highlights:

- Importance of monitoring repeated endpoint access
- Need for strong authorization checks
- Immediate containment after confirmed exploitation

---

## 🔎 Full Technical Breakdown

This README only covers IOCs and summary artifacts.

For full log analysis, investigation reasoning, validation steps, and SOC decision-making process:

👉 **Read the complete blog post here:**  
[Full HASHNODE_BLOG_LINK](https://rideshcyber.hashnode.dev/soc169-possible-idor-attack-detected-walkthrough-eventid-119)

---

### Connect & Learn

If you're documenting your SOC journey or learning blue team operations, follow along for more real-world alert investigations.
