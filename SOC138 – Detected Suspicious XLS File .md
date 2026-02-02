# 🚨 SOC138 – Suspicious XLS File Execution (EventID: 77)

## 📌 Alert Summary
A **suspicious XLS spreadsheet** containing **malicious macros** was executed on the host **SOFIA**, resulting in **unauthorized access** and **Command-and-Control (C2) communication**.  
The host device was **successfully contained**, but further mitigation actions are recommended to prevent data loss.

---

## 🖥️ Affected Host Details
- **Hostname:** SOFIA  
- **Source IP:** 172.16.17.56  
- **Event ID:** 77  
- **Execution Time:** Mar 13, 2021 – 08:20 PM  

---

## 📂 Malicious File Details
- **File Name:** `ORDER SHEET & SPEC.xlsm`
- **File Type:** Excel Macro-enabled Spreadsheet
- **File Size:** 2.66 MB
- **File Hash (MD5):** `7ccf88c0bbe3b29bf19d877c4596a8d4`

⚠️ The file contained **malicious macros** designed to establish **C2 communication**.

---

## 🌐 Network & C2 Indicators
- **Suspicious IP Address:** `177.53.143.89`
- **Activity Observed:**  
  - Outbound connection detected  
  - Unauthorized access achieved  
  - Indicators consistent with **Command & Control behavior**

---

## 🔍 Threat Intelligence Verdict
- **VirusTotal Result:** Malicious  
- **Threat Classification:**  
  - Macro-based malware  
  - C2-enabled payload  
  - Potential data compromise risk  

---

## 🛡️ Containment & Response
- ✅ Host device **contained / quarantined**
- ⚠️ Additional actions recommended:
  - Credential review
  - Endpoint hardening
  - Network monitoring for related IOCs

---

## 📎 Indicators of Compromise (IOCs)
| Type | Value |
|----|------|
| File Hash (MD5) | `7ccf88c0bbe3b29bf19d877c4596a8d4` |
| Malicious IP | `177.53.143.89` |
| File Name | `ORDER SHEET & SPEC.xlsm` |
| Host IP | `172.16.17.56` |

---

## 📝 Analyst Notes
- The malicious spreadsheet leveraged **macro execution** to gain access.
- C2 traffic confirms **active attacker interaction**.
- Although the host was already contained, alert workflow still required containment confirmation.

---

## 🔗 Full Investigation Walkthrough
👉 **Detailed SOC investigation with screenshots and reasoning:**  
[Hashnode Blog – SOC138 Walkthrough](https://soc138-detected-suspicious-xls-file.hashnode.dev/soc138-detected-suspicious-xls-file-soc-alert-walkthrough?showSharer=true)

---


