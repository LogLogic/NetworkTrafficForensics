# Network Traffic & Forensics

This repository showcases real-world network forensics and traffic analysis projects using Wireshark. Each project simulates SOC analyst workflows—packet inspection, protocol analysis, IOC extraction, and attack chain reconstruction.

These investigations demonstrate how network captures can be leveraged for threat hunting, malware detection, and incident response.

---

## 📡 Projects

### 🕵️‍♀️ Fake Antivirus Redirect Campaign (Wireshark)
📝 [Read the Report](https://github.com/LogLogic/NetworkTrafficForensics/blob/main/FakeAntivirusRedirectCampaign/fake_av_redirect_investigation_report.md)

Case study analyzing a multi-stage browser-based attack captured in a PCAP file. Involves JavaScript injection, chained redirects across attacker-controlled `.tk` domains, and a final tech support scam landing page. Includes:

- HTTP inspection and JavaScript analysis  
- TCP stream tracing across multiple redirect stages  
- IOC extraction: domains, IPs, and scam phone numbers  
- Full SOC-style investigation report with screenshots

---

### 🕵️‍♂️ Malware EXE Download Analysis (Wireshark)  
📝 [Read the Report](https://github.com/LogLogic/NetworkTrafficForensics/blob/main/MalwareEXEDownloadAnalysis/malware_exe_download_investigation_report.md)

Investigation of a direct malware executable download captured in network traffic. Features a Windows host downloading a malicious PE file over HTTP, file extraction and hashing, and post-download network behavior analysis. Includes:

- HTTP GET and response inspection  
- Extraction and hash verification of malware executable   
- Detailed step-by-step guide with commands and screenshots  
- Full SOC-style investigation report  
