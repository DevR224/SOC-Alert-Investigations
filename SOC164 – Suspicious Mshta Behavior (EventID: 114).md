# 🚨 SOC164 – Suspicious Mshta Behavior (EventID: 114)

---

## 📌 Alert Overview

- **Platform:** LetsDefend
- **Alert Name:** SOC164 – Suspicious Mshta Behavior
- **Event ID:** 114
- **Hostname:** Roberto
- **Host IP:** 172.16.17.38
- **Related Binary:** mshta.exe
- **Binary Path:** C:\Windows\System32\mshta.exe

---

## 🧠 Incident Summary

On March 05, 2022 at 10:29 AM, a suspicious C2 (Command and Control) connection was established between the internal host **Roberto (172.16.17.38)** and the external attacker IP:

```
193.142.58.23
```

Investigation revealed that the attacker abused a legitimate Windows LOLBin (`mshta.exe`) to execute a malicious HTA file:

```
C:\Users\Roberto\Desktop\Ps1.hta
```

The HTA file was executed using:

```
C:\Windows\System32\mshta.exe C:\Users\Roberto\Desktop\Ps1.hta
```

The malicious HTA file was used to gather data and collect emails from Microsoft Outlook.

The host system was quarantined and the alert was escalated to a Tier 2 analyst for further incident handling.

---

# ⚠️ Indicators of Compromise (IOCs)

## 🖥️ Affected Host

```
Hostname: Roberto
IP Address: 172.16.17.38
```

---

## 🌐 Command & Control (C2) IP

```
193.142.58.23
```

- External attacker-controlled IP
- Established outbound communication with internal host

---

## 🧩 Abused LOLBin

```
C:\Windows\System32\mshta.exe
```

- Legitimate Windows binary
- Used for executing HTA (HTML Application) files
- Commonly abused in LOLBin attacks

---

## 📄 Malicious File

```
C:\Users\Roberto\Desktop\Ps1.hta
```

**MD5 Hash:**

```
6685c433705f58c5535789234db0e5a
```

---

## 🧾 Suspicious Command Line

```
C:\Windows\System32\mshta.exe C:\Users\Roberto\Desktop\Ps1.hta
```

---

# 🔎 Observed Malicious Behavior

- LOLBin abuse via mshta.exe
- Execution of malicious HTA file
- Outbound C2 communication established
- Data gathering activity (including Outlook email collection)
- Potential data exfiltration

---

# 🎯 MITRE ATT&CK Mapping

- T1218.005 – Signed Binary Proxy Execution: Mshta
- T1071 – Application Layer Protocol (C2 Communication)
- T1005 – Data from Local System
- T1114 – Email Collection
- T1105 – Ingress Tool Transfer

---

# 🛑 Response Actions

- Analyzed process execution logs
- Identified malicious HTA execution
- Confirmed outbound C2 communication
- Quarantined affected host
- Escalated to Tier 2 for further investigation
- Documented artifacts and IOCs

---

# 📖 Full Investigation Walkthrough

For the complete step-by-step analysis:

👉 [Full Hashnode Blog Here](https://rideshcyber.hashnode.dev/soc164-suspicious-mshta-behavior-walkthrough-eventid114)

---

# 📌 Key Takeaways

- Legitimate binaries like `mshta.exe` are frequently abused in LOLBin attacks.
- HTA file execution should be closely monitored in enterprise environments.
- C2 communication is a strong indicator of active compromise.
- Early containment is critical to prevent data exfiltration.
- Proper IOC documentation improves threat hunting capability.

---

## 🧑‍💻 About This File

This File documents real-world SOC investigations with focus on:

- LOLBin abuse detection
- Command execution analysis
- C2 identification
- IOC extraction
- Incident response workflow
