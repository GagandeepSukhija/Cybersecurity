---
ID: "20250725201631"
---
As IT and cybersecurity companies gather heaps of data that could be used for intelligence and threat analysis. To solve this issue, Cisco assembled a large team of security practitioners to provide actionable intelligence, threat indicators and protection against emerging threats with data collected from their own products. This team is called Talos.

Talos has 6 main teams (quoted from TryHackMe):
- **Threat Intelligence & Interdiction:** Quick correlation and tracking of threats provide a means to turn simple IOCs into context-rich intel.
- **Detection Research:** Vulnerability and malware analysis is performed to create rules and content for threat detection.
- **Engineering & Development:** Provides the maintenance support for the inspection engines and keeps them up-to-date to identify and triage emerging threats.
- **Vulnerability Research & Discovery:** Working with service and software vendors to develop repeatable means of identifying and reporting security vulnerabilities.
- **Communities:** Maintains the image of the team and the open-source solutions.
- **Global Outreach:** Disseminates intelligence to customers and the security community through publications.

Their Open Source Solution:
https://www.talosintelligence.com/reputation_center

You are greeted with a dashboard that displays a reputation lookup of emails globally, allowing you to find out more information on each such as IP and hostname address, their classification (legitimate, spam, malware). It also displays their volume on the day and the type.

There are also other resources available such as:
- Vuln Information:
	- Disclosed and zero day vulns with CVE and CVSS scores. Details of the vuln are provided with reports and a timeline of how long it took for the report to get published. Microsoft vulns are also provided with SNORT rules.
- Reputation Centre:
	- Like VirusTotal, checks the hash. For email and spam data, there is an “Email and Spam Data” tab.
