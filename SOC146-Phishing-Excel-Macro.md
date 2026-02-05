# 🚨 SOC146 – Phishing Mail Detected (Excel 4.0 Macros)
**Event ID:** 93  
**Platform:** LetsDefend  
**Alert Type:** Phishing → Malicious Attachment  
**Severity:** High  

---

## 🧾 Alert Summary
A phishing email containing a **malicious Excel attachment using Excel 4.0 macros** was detected and delivered to the host.  
The attachment was confirmed **malicious (Spyware)** and was **opened by the user**, leading to host compromise.

---

## 🧠 Key Findings
- 📧 Suspicious email with **no legitimate context**
- 📎 Malicious Excel attachment leveraging **Excel 4.0 macros**
- 🦠 Malware classified as **Spyware**
- 🖥️ Email **delivered and accessed** on the host
- 🔓 Attachment **opened**
- 🔒 Host **contained** to prevent further impact
- ✅ Alert confirmed as **True Positive**

---

## 🧩 Indicators of Compromise (IOCs)

### 📎 File Hash
11f44531fb088d31307d87b01e8eabff


### 📧 Email Artifacts
Sender Email : trenton@tritowncomputers.com

Recipient Email: lars@letsdefend.io

SMTP IP : 24.213.228.54
Sent Time : Jun 13, 2021 – 02:11 PM

### 🦠 Malware Details

Malware Type : Spyware
Vector : Excel 4.0 Macros
Source : Phishing Email Attachment

---

## 🛡️ Response Actions
- 🗑️ Malicious email **deleted**
- 🔒 Affected host **contained**
- 🧾 Artifacts documented
- 📝 Analyst notes added
- ✅ Alert **closed as True Positive**

---

## 📚 Full Investigation Walkthrough
For a **step-by-step SOC analysis with screenshots and reasoning**, read the full blog:

🔗 **Hashnode Blog:**  
👉 *SOC146 Hashnode blog link here*

---

## 🎯 Purpose of This File
This document serves as:
- 📌 Proof of **hands-on SOC investigation**
- 📊 Quick IOC reference
- 👀 Recruiter-friendly alert summary

> Detailed analysis is intentionally kept on the blog for readability.

---

**Author:** Ridesh Bijwe  
**Focus:** SOC Analysis | Incident Response | Blue Team  

