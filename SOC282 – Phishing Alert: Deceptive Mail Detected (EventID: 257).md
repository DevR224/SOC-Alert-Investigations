# 🚨 SOC282 – Phishing Alert: Deceptive Mail Detected (EventID: 257)

---

## 📌 Alert Overview

- **Platform:** LetsDefend
- **Alert Name:** SOC282 – Phishing Alert: Deceptive Mail Detected
- **Event ID:** 257
- **SMTP IP Address:** 103.80.134.63
- **Source Email:** free@coffeeshoop.com
- **Destination Email:** felix@letsdefend.io
- **Destination IP:** 172.16.20.151
- **Affected Host:** Felix

---

## 🧠 Incident Summary

On May 13, 2024 at 09:22 AM, host **Felix** received a phishing email claiming a free coffee voucher.

The email contained a ZIP attachment.

Upon investigation:

- The ZIP file contained a malicious URL
- The URL was associated with malware
- The user interacted with the content
- The attacker gained access to the host system
- Persistence and privilege escalation activities were observed

The host was contained, and the alert was escalated to Tier 2 for further incident handling.

---

# ⚠️ Indicators of Compromise (IOCs)

## 🌐 Malicious SMTP IP

```
103.80.134.63
```

- Associated with phishing email delivery
- External mail server

---

## 📧 Malicious Email Address

```
free@coffeeshoop.com
```

- Phishing lure: Free coffee voucher
- Social engineering technique used

---

## 🗂️ Malicious Attachment

```
free-coffee.zip
```

- ZIP archive containing malicious content
- Embedded malicious URL

---

## 🖥️ Targeted Host

```
Hostname: Felix
Destination IP: 172.16.20.151
```

---

# 🔎 Observed Malicious Behavior

- Phishing email delivery
- Malicious ZIP attachment
- URL reputation flagged as malicious
- User interaction confirmed
- Host access established
- Persistence mechanisms initiated
- Privilege escalation attempts observed

---

# 🎯 MITRE ATT&CK Mapping

- T1566.001 – Phishing: Spearphishing Attachment
- T1204 – User Execution
- T1105 – Ingress Tool Transfer
- T1547 – Persistence
- T1068 – Privilege Escalation

---

# 🛑 Response Actions

- Email analyzed and confirmed malicious
- Malicious email deleted
- User interaction confirmed via logs
- Host system contained
- Artifacts documented
- Escalated to Tier 2 for further incident response

---

# 📖 Full Investigation Walkthrough

For the complete step-by-step blog analysis:

👉 [Full Hashnode Blog Here](https://rideshcyber.hashnode.dev/soc282-phishing-alert-deceptive-mail-detected-walkthrough-eventid257)

---

# 📌 Key Takeaways

- ZIP attachments in phishing emails are high risk.
- Always verify file reputation before concluding.
- User interaction significantly increases incident severity.
- Containment should be immediate once compromise is suspected.
- Proper documentation supports escalation and tracking.

---

## 🧑‍💻 About This Repository

This repository documents real-world SOC alert investigations with focus on:

- IOC extraction
- Phishing analysis
- Threat detection workflows
- Incident response methodology
