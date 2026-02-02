# SOC202 – FakeGPT Malicious Chrome Extension (EventID:153)

## 🔍 Alert Summary
A malicious Chrome extension disguised as a FakeGPT tool was executed on the host, resulting in restricted Windows Defender privileges and outbound communication to a suspicious external domain. Endpoint behavior and threat intelligence confirmed malicious activity, and the host was contained.

---

## 🚨 Key Indicators of Compromise (IOCs)

### File
- **Name:** hacfaophiklaeolhnmckojjjbnappen.crx  
- **Path:** `C:\Users\LetsDefend\Download\`  
- **SHA-256:** `7421f9abe5618a0d517861f4709df53292a5f137053a227bfb4eb8e152a4669`

### Network
- **Domain:** `www.chatgptforgoogle.pro`
- **IP Address:** `52.76.101.124`
- **Direction:** Outbound

---

## 🛡️ Response Action
- Host was isolated using endpoint security controls
- Malicious extension execution blocked

---

## 📖 Full Walkthrough
➡️ **Detailed investigation, log analysis, and reasoning available here:**  
🔗 *Hashnode Blog:*  
`https://rideshcyber.hashnode.dev/soc202-fakegpt-malicious-chrome-extension`

---

## 🧠 Skills Demonstrated
- IOC Identification  
- Endpoint Threat Analysis  
- SOC Alert Triage  
- Incident Summarization  
