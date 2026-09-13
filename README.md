# OSINT-Based Threat Intelligence Assessment
This project provides a comprehensive Cyber Threat Intelligence (CTI) assessment of Klarna using ethical, passive **OSINT** techniques. It evaluates Klarna’s digital footprint, phishing exposure, impersonation risks, and publicly visible infrastructure. The goal is to understand external threats without interacting with or testing Klarna’s internal systems.

## Table of Contents
- Project Overview
- Network Topology
- Tools and Technologies
- Configuration Steps
- Results and Findings
- Author

## Project Overview
This project investigates Klarna’s exposure to phishing, impersonation, and fraud activities using publicly available open‑source intelligence. The assessment identifies legitimate and suspicious infrastructure, evaluates email authentication results, and maps attacker behaviour using the **MITRE ATT&CK** framework. The report concludes that Klarna’s risk level is **Medium**, driven primarily by brand impersonation attempts rather than weaknesses in Klarna’s own systems.

## Network Topology
- **Primary Domain:** klarna.com  
- **Key Subdomains:**  
  - app.klarna.com  
  - checkout.klarna.com  
  - merchant.klarna.com  
  - api.klarna.com  
- **Hosting Providers:**  
  - AWS  
  - Cloudflare  
  - DigitalOcean  
  - Hetzner  
  - Bird.com (SparkPost for email)  
- **Legitimate Email IP:** 199.15.226.148  
- **Malicious Phishing IP:** 109.202.24.52 (reported for phishing, spam, hacking, brute‑force)  
- **Archived Infrastructure:** Historical Klarna pages accessible via the Wayback Machine  
- **Suspicious Domains:**  
  - `54upr.rosreestr.ru`  
  - `avantel.ru`  

## Tools and Technologies
- **Google Dorks**
- **theHarvester**
- **Shodan**
- **MXToolbox**
- **VirusTotal**
- **AbuseIPDB**
- **Wayback Machine**
- **WHOIS Lookup**
- **MITRE ATT&CK Framework**
- **Public DNS Records**
- **Public Breach Databases**

## Configuration Steps
1. Conduct OSINT planning to define intelligence objectives and scope.
2. Use Google Dorks to identify exposed Klarna-related files and indexed content.
3. Run `theHarvester` to enumerate subdomains, IPs, and email-related metadata.
4. Analyse archived Klarna pages using the Wayback Machine.
5. Inspect exposed services using Shodan without performing exploitation.
6. Perform email header analysis using MXToolbox to verify SPF, DKIM, and DMARC.
7. Check IP reputation using VirusTotal and AbuseIPDB.
8. Review WHOIS records to confirm domain ownership.
9. Categorise URLs, IPs, and documents into legitimate, suspicious, and archived groups.
10. Map attacker behaviour to MITRE ATT&CK techniques.
11. Compile findings into a structured CTI report.

## Results and Findings
- **Active Phishing Attempts:**  
  Suspicious emails impersonating Klarna failed SPF, DKIM, and DMARC checks. The sender IP had multiple abuse reports, confirming malicious activity.

- **Brand Impersonation:**  
  Attackers used foreign infrastructure and cloned Klarna’s archived pages to create convincing phishing portals.

- **Infrastructure Exposure:**  
  Klarna’s large digital footprint across multiple cloud providers increases opportunities for attackers to spoof or imitate services.

- **Data Leakage Indicators:**  
  Publicly accessible Klarna documents (fraud policies, merchant rules, security guidelines) could help attackers craft realistic phishing messages.

- **Risk Level:**  
  - **Financial Risk:** Medium  
  - **Reputational Damage:** Medium  
  - **Customer Trust Impact:** Medium  
  - **Regulatory Exposure:** Low–Medium  

## Author
**Abeeb Salaudeen**  
Email: salaudeenabeeb21@gmail.com  
