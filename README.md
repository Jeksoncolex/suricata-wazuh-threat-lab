# 🛡️ SOC Automation Lab: Suricata IDS + Wazuh SIEM + VirusTotal

## 📋 Executive Summary
This lab showcases the deployment of a modernized **Security Operations Center (SOC)** workflow. By integrating **Suricata (Intrusion Detection)** with **Wazuh (SIEM)** and automating threat intelligence via the **VirusTotal API**, I successfully built a system that detects, aggregates, and validates network threats in real-time.

---

## 🛠️ Technical Stack
- **OS:** Kali Linux (Attacker/Monitoring)
- **IDS:** Suricata (Signature-based detection)
- **SIEM:** Wazuh (Log aggregation & Alerting)
- **Threat Intel:** VirusTotal (Automated Hash/IP Validation)
- **Environment:** VS Code & GitHub for Documentation

---

## 🏗️ Project Architecture & Workflow
The lab follows a structured data pipeline to ensure no threat goes unvalidated:
1. **Detection:** Suricata monitors network traffic for known malicious signatures.
2. **Aggregation:** Wazuh Manager ingests Suricata logs (`eve.json`) for centralized viewing.
3. **Enrichment:** Wazuh triggers an automated API call to VirusTotal for any suspicious file hashes detected.
4. **Action:** The analyst reviews enriched alerts on the Wazuh Dashboard for final triage.

---

## 🚀 Implementation Highlights

### 1. Suricata Deployment
Configured Suricata for high-performance network monitoring and ensured seamless logging for SIEM consumption.
```bash
sudo apt update && sudo apt install suricata -y
sudo systemctl enable --now suricata
```

### 2. SIEM & Threat Intel Integration
Connected Wazuh to monitor the Suricata output directory and configured the `ossec.conf` to trigger VirusTotal lookups, transforming raw logs into actionable intelligence.

---

## 🖼️ Visual Evidence (SOC Dashboard)

### 🚨 Threat Simulation & Monitoring
*Real-time validation of network alerts within the SOC environment.*
![Terminal Simulation](screenshots/Terminal-Threat-Simulation.png)
![VM Login](screenshots/VM-Login-Screen.png)

### 📊 SIEM Analysis (Wazuh)
*Visualizing alert density and deep-diving into specific intrusion metadata.*
![Wazuh Dashboard](screenshots/Wazuh-Dashboard-Alerts.png)
![Wazuh Alert Details](screenshots/Wazuh-Alert-Details.png)

### 🔍 Threat Validation (VirusTotal)
*Automated verification of malicious indicators using global threat intelligence.*
![VirusTotal Results](screenshots/VirusTotal-Detection-Results.png)
![Wazuh Integration Logs](screenshots/Wazuh-Integration-Logs.png)

---

## 🧠 Key Findings & SOC Skills
- **Log Parsing:** Mastered the flow of data from `eve.json` to Wazuh indexes.
- **Incident Triage:** Learned to differentiate between a raw IDS hit and a validated threat.
- **Troubleshooting:** Overcame Wazuh manager timeouts and log-forwarding permission issues.

---

## 👨‍💻 Author
**Sunday Ojeka**
*Aspiring SOC Analyst | Cybersecurity Specialist*
Focused on Blue Team Operations and Security Automation.
