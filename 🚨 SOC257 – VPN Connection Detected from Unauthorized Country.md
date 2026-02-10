# SOC257 – VPN Connection Detected from Unauthorized Country (EventID-225)

## 🧠 Alert Summary
- **Alert ID:** SOC257  
- **Severity:** Low  
- **Category:** Unauthorized Access / VPN Anomaly  
- **Platform:** LetsDefend SOC  
- **Status:** True Positive (No System Compromise)

This alert was triggered due to repeated VPN authentication attempts from an **unauthorized country**, indicating a potential brute-force or credential-stuffing attempt.

---

## 🎯 Investigation Outcome
- Multiple failed VPN login attempts detected  
- Source IP identified as **external and malicious**  
- MFA (OTP) successfully prevented account compromise  
- No unauthorized access gained  
- No data exposure or system impact

---

## 📌 Indicators of Compromise (IOCs)

### 🌐 Malicious Source IP
- **IP Address:** `113.161.158.12`
- **Geolocation:** Vietnam
- **Reputation:** Malicious (VirusTotal flagged)

### 🔌 Network Indicator
- **Destination Port:** `443` (HTTPS / VPN)

### 🖥️ Target Host
- **Hostname:** `Monica`

---

## 🛡️ Mitigation & Response
- Alert validated as **True Positive**
- No host isolation required
- Evidence preserved
- MFA confirmed effective against attack
- Standard eradication and recovery steps followed

---

## 📖 Full Investigation Walkthrough
👉 **Read the complete SOC analysis here:**  
🔗 *[Hashnode-Article ](https://rideshcyber.hashnode.dev/soc257-vpn-connection-detected-from-unauthorized-country-eventid225?showSharer=true)*  

---

## 🧩 Skills Demonstrated
- Log analysis & correlation  
- IP reputation analysis  
- VPN & MFA security assessment  
- SOC playbook-driven investigation  
- Incident response decision-making

---

⭐ *This repository is part of my ongoing SOC alert investigation series focused on real-world detection and response scenarios.*
