# Wireshark Traffic Analysis – Multi-Stage Fake Antivirus Redirect Campaign

This project analyzes a real-world browser-based redirect attack captured in a PCAP file. The attack involves malicious JavaScript injection on a legitimate site, chained redirects to attacker-controlled `.tk` domains, and a final fake antivirus tech support scam landing page.

---

## Project Overview

**Goal:**  
Analyze network traffic to understand the flow of a multi-stage redirect attack, extract Indicators of Compromise (IOCs), and document the attack lifecycle.

**Data:**  
PCAP file from [malware-traffic-analysis.net (2018-01-08)](https://www.malware-traffic-analysis.net/2018/01/08/index.html) capturing HTTP requests, redirects, and injected JavaScript.

**Tools:**  
Wireshark for packet capture analysis  
Markdown for documentation  

---

## Tools & Features Used

- Wireshark TCP stream and HTTP inspection  
- Filtering for HTTP requests and redirects  
- JavaScript code extraction and analysis  
- IOC extraction and documentation  
- Structured reporting with Markdown

---

## Analysis Summary

1. Victim visits legitimate website `proactivo.com.pe`  
2. HTTP response contains injected malicious JavaScript causing browser redirect  
3. Victim’s browser follows redirect to attacker domain `raksupp0rt0701234567890[.]tk`  
4. Redirect server responds with HTTP 302 redirect to scam domain `tehcallinghere07012345[.]tk`  
5. Final landing page urges victim to call fraudulent tech support phone number

---

## Indicators of Compromise

| Type               | Value                          |
|--------------------|--------------------------------|
| Victim IP          | `10.1.8.101`                   |
| Compromised Site   | `proactivo.com.pe`             |
| Redirect Domain 1  | `raksupp0rt0701234567890[.]tk` |
| Redirect Server IP | `204.155.28.5`                 |
| Redirect Domain 2  | `tehcallinghere07012345[.]tk`  |
| Scam Phone Number  | `888-794-9521`                 |

---

## Investigation Report

A detailed SOC-style incident analysis documenting detection, tracking, and forensic insights into the multi-stage redirect attack.

→ [View Full Investigation Report](fake_av_redirect_investigation_report.md)


---

## Disclaimer

Malicious domains are defanged with `[.]` to prevent accidental access. This project is for educational and professional development only.
