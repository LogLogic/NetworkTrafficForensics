# 🕵️‍♀️ Wireshark Traffic Analysis – Multi-Stage Fake Antivirus Redirect Campaign

This project investigates a real-world browser-based redirect attack captured in a PCAP file. The attack involves a compromised website injecting malicious JavaScript, which initiates chained redirects to attacker-controlled `.tk` domains, ultimately landing the user on a fake antivirus tech support scam page.

> 📅 **Case Date:** January 8, 2018  
> 📁 **PCAP Source:** [malware-traffic-analysis.net](https://www.malware-traffic-analysis.net/2018/01/08/index.html)  
> 📖 **Related Report:** [SANS ISC Diary](https://isc.sans.edu/diary/Fake+antivirus+pages+popping+up+like+weeds/23207)

---

## 🧠 Skills Demonstrated

- Network forensics with Wireshark  
- TCP stream and HTTP inspection  
- Malicious JavaScript analysis  
- Multi-stage redirection flow analysis  
- IOC extraction and documentation  
- Threat modeling and report writing

---

## 📋 Project Contents

| File | Description |
|------|-------------|
| `fake_av_redirect_investigation_report.md` | Full technical report detailing the staged redirect campaign |
| `screenshots/` | Visuals of HTTP requests, redirects, JavaScript, and traffic filters |
| `README.md` | Project summary and reference metadata |

---

## 🧾 Summary of Attack Flow

1. Victim visits legitimate site `proactivo.com.pe`
2. HTTP response injects JavaScript to redirect to `raksupp0rt0701234567890[.]tk`
3. That server responds with a 302 redirect to `tehcallinghere07012345[.]tk`
4. The final page displays a fake AV scam urging the victim to call a phone number

---

## 🔍 Indicators of Compromise

| Type               | Value                          |
|--------------------|--------------------------------|
| Victim IP          | `10.1.8.101`                   |
| Compromised Site   | `proactivo.com.pe`             |
| Redirect Domain 1  | `raksupp0rt0701234567890[.]tk` |
| Redirect Server IP | `204.155.28.5`                 |
| Redirect Domain 2  | `tehcallinghere07012345[.]tk`  |
| Scam Phone Number  | `888-794-9521`                 |

---

## ⚠️ Disclaimer

All malicious domains in this report have been intentionally defanged (e.g. using `[.]`) to prevent accidental access. Do **not** attempt to visit them. This project is for educational and professional development purposes only.

---

## 🛠️ Tools Used

- Wireshark  
- Malware-Traffic-Analysis.net case data  
- Markdown for reporting

