# Security Monitoring & Incident Response Lab | Wazuh + Suricata

**Author:** Pedro Gonçalves  
**Project:** Operational Cybersecurity — Technical Lab Portfolio  
**Documentation:** Portuguese | **README:** English

## Project overview

This project documents a virtual cybersecurity laboratory designed to explore **centralized security monitoring, host-based detection, network intrusion detection, and incident response** across Linux and Windows systems.

The lab uses **Wazuh** to collect and analyze endpoint security events and **Suricata** to inspect network activity. Controlled exercises cover file-integrity changes, antivirus test-file alerts, reconnaissance detection, web-traffic analysis, and automated response rules. The full report includes setup notes, configuration examples, screenshots, log evidence, and troubleshooting.

> **Lab scope:** All security testing described here is intended for an isolated, authorized environment. The report records training exercises; it is not a claim of production deployment or independent security certification.

## Lab architecture

The environment consists of five virtual machines connected to a private lab network, with NAT connectivity where required:

| System | Role | Main components |
| --- | --- | --- |
| Linux Mint / Ubuntu Server | Central monitoring server | Wazuh Manager and dashboard |
| Debian 13 | Monitored Linux endpoint | Wazuh Agent, Suricata |
| Rocky Linux 10 | Monitored Linux endpoint / web target | Wazuh Agent, Suricata, web service |
| Windows 10/11 | Monitored Windows endpoint | Wazuh Agent, Windows event monitoring |
| Kali Linux / Parrot OS | Authorized test workstation | Nmap, OWASP ZAP and other lab testing tools |

The accompanying PDF contains the detailed architecture illustration and the addressing and hostname configuration used in the exercises.

## Main objectives

1. **Deploy centralized monitoring:** configure the Wazuh server and enroll Windows and Linux agents; verify their connection and reporting status.
2. **Monitor file integrity (FIM):** detect file creation, modification, and deletion in selected Linux and Windows directories.
3. **Investigate test-file detections:** examine alerts produced using the harmless EICAR antivirus test string, with related VirusTotal integration and response workflows where configured.
4. **Detect network reconnaissance:** generate authorized Nmap scans and review detection and response events.
5. **Monitor web security events:** configure lab web services, analyze traffic and alerts, and document OWASP ZAP testing.
6. **Explore automated responses:** apply time-limited IP blocking and file-response rules in controlled scenarios; validate actions against event logs.
7. **Organize endpoints:** create separate Windows and Linux agent groups and customize monitoring policies.

## Technologies and tools

`Wazuh` · `Suricata` · `Linux` · `Windows` · `Kali Linux` · `Debian 13` · `Rocky Linux` · `Nmap` · `OWASP ZAP` · `VirusTotal` · `FIM` · `Active Response` · `SIEM` · `IDS` · `Log Analysis`

## Documentation and evidence

The technical report includes:

- Installation and configuration procedures for the monitoring platform and agents.
- Endpoint and network-service configuration examples.
- Security-event screenshots, detection rules, and log excerpts.
- Test procedures and observed results for the different lab scenarios.
- Discussion of monitoring coverage, limitations, and response validation.

**[View the complete illustrated technical report (PDF)](UFCD_9195_Wazuh_Suricata_Pedro_Goncalves_Com_Imagem.pdf)**

To keep the link working, upload the PDF to the **same directory** as this `README.md` and preserve its filename.

## Skills demonstrated

- Security monitoring and SIEM/XDR lab administration
- Linux and Windows endpoint telemetry
- File Integrity Monitoring (FIM)
- Intrusion detection with Suricata
- Log analysis and alert investigation
- Detection engineering and automated response validation
- Security testing in authorized lab environments
- Technical documentation and evidence collection

## Responsible use and disclosure

This repository is for **educational and defensive cybersecurity purposes**. Perform scans and attack simulations only against systems you own or are explicitly authorized to test. Before publishing or reusing screenshots and configurations, review them for personal data, credentials, identifying details, and other sensitive information.

## Author

**Pedro Gonçalves**  
Cybersecurity · Network Engineering · System Administration  
[GitHub profile](https://github.com/PedroGoncalves28286)
