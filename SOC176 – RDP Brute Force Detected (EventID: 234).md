# 🚨 SOC176 – RDP Brute Force Detected (EventID: 234)

---

## 📌 Alert Overview

- **Platform:** LetsDefend
- **Alert Name:** SOC176 – RDP Brute Force Detected
- **Event ID:** 234
- **Protocol:** RDP (Remote Desktop Protocol)
- **Destination Hostname:** Matthew
- **Destination IP:** 172.16.17.148
- **Source IP:** 218.92.0.56

---

## 🧠 Incident Summary

On March 07, 2024 at 11:44 AM, an external IP address launched multiple RDP authentication attempts against internal systems.

The attacker attempted login using several usernames:

- guest
- admin
- sysadmin
- Matthew

The brute force attempt was successful against the account **Matthew**, resulting in unauthorized remote access.

Following successful access, malicious actions were performed to establish persistence and potentially escalate privileges.

The host system was contained as part of the incident response process.

---

# ⚠️ Indicators of Compromise (IOCs)

## 🌐 Malicious Source IP

```
218.92.0.56
```

- Origin: External
- Reputation: Reported in abuse databases
- Activity: RDP brute force attempts

---

## 🖥️ Targeted Host

```
Hostname: Matthew
IP Address: 172.16.17.148
Protocol: RDP (Port 3389)
```

---

## 🔑 Targeted Usernames

```
guest
admin
sysadmin
Matthew
```

Only the account **Matthew** was successfully compromised.

---

# 🔎 Observed Malicious Behavior

- High-frequency RDP login attempts
- Multiple username enumeration attempts
- Successful authentication
- Remote session establishment
- Post-authentication activity indicating:
  - Persistence attempts
  - Potential privilege escalation

---

# 🎯 MITRE ATT&CK Mapping

- T1110 – Brute Force
- T1021.001 – Remote Services (RDP)
- T1078 – Valid Accounts
- T1059 – Command Execution
- T1547 – Persistence Mechanisms

---

# 🛑 Response Actions

- Verified IP reputation
- Analyzed raw authentication logs
- Confirmed successful compromise
- Contained affected host
- Documented artifacts
- Closed alert after validation

---

# 📖 Full Investigation Write-up

For the complete step-by-step investigation and analysis walkthrough:

👉 [Full Hashnode Blog Here](https://rideshcyber.hashnode.dev/soc176-rdp-brute-force-detected-walkthrough-eventid-234)

---

# 📌 Key Takeaways

- Repeated RDP login attempts should always trigger investigation.
- External IP reputation validation strengthens detection confidence.
- Successful brute force attempts require immediate containment.
- Monitoring authentication logs is critical for early detection.

---

## 🧑‍💻 About This Repository

This repository documents real-world SOC alert investigations, focusing on:

- IOC extraction
- Log analysis
- Threat detection methodology
- Incident response workflow
