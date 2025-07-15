# Network Traffic & Forensics

This repository showcases real-world network forensics and traffic analysis projects using Wireshark. Each project simulates SOC analyst workflows—packet inspection, protocol analysis, IOC extraction, and attack chain reconstruction.

These investigations demonstrate how network captures can be leveraged for threat hunting, malware detection, and incident response.

---

## 📡 Projects

### 🕵️‍♀️ Fake Antivirus Redirect Campaign (Wireshark)
📝 [Read the Report](NetworkTrafficForensics/fake_av_redirect_investigation_report.md)

Case study analyzing a multi-stage browser-based attack captured in a PCAP file. Involves JavaScript injection, chained redirects across attacker-controlled `.tk` domains, and a final tech support scam landing page. Includes:

- HTTP inspection and JavaScript analysis  
- TCP stream tracing across multiple redirect stages  
- IOC extraction: domains, IPs, and scam phone numbers  
- Full SOC-style investigation report with screenshots  
