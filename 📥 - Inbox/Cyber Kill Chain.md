---
ID: "20250711192250"
---
# Overview:
A military concept that defines the structure of an attack used by adversaries. Lockheed Martin established the framework for the cybersecurity industry in 2011. To succeed, the attacker would need to go through all the phases of the Kill Chain. 

Understanding how the Kill Chain works will help you better protect against ransomware attacks, security breaches and APTs. You can use the Kill Chain to assess your network and system security by identifying missing controls and closing certain security gaps based on the company’s infrastructure. Furthermore, by understanding the chain as an SOC Analyst, Security Researcher, Threat Hunter or Incident Responder; you’ll be able to better recognise the intrusion attempts and understand the intruder’s goals and objectives. 

By understanding the Kill Chain and being able to identify where an attacker is in the Kill Chain, you’ll know how to break it.

![[Pasted image 20250711192724.png]]

# The Cyber Kill Chain:
1) Reconnaissance
2) Weaponisation
3) Delivery
4) Exploitation
5) Installation
6) Command & Control
7) Actions on Objectives

# Reconnaissance:
Discovering and collecting information on the system and the victim. [[OSINT]] (Open Source Intelligence) also falls under reconnaissance and is the first step an attacker needs to complete to carry out the next phases of the attack.

# Weaponisation:
An attacker creates a [[Weaponiser]]. Most attackers usually use automated tools to generate the malware or purchase it off the DarkWeb. Sophisticated attackers or nation-sponsored APTs would can write their custom malware to make the malware sample unique and evade detection on the target.

In this Phase the attacker would:
- Create an Infected MS Office document with a malicious macro or [[VBA]] scripts.
- Create Sophisticated worm on a USB and then distribute them in public.
- Choose C2 techniques to execute commands on the victim’s device to deliver more payloads.
- Select a backdoor implant (how to access the system and bypassing security mechanisms)

# Delivery:
The attacker chooses the method to transmit the payload. This could be a phishing email, distributing an infected USB or a [[Watering Hole Attack]]. [[Case Study - BadUSB Mailed to Companies]].


# Exploitation:
- Following this scenario of a Maldoc attack using MS Office applications, the attacker sends 2 emails, one with a phishing link to a face 365 login page and another with a macro attachment that’ll execute ransomware. The attacker obtains 2 victims.
- Once he’s gained access, they can exploit software, the system, exploit server-based vulnerabilities to escalate privileges or use [[Lateral Movement]].
- To learn about server/web-based vulnerabilities, go to the following:
	- https://tryhackme.com/room/owasptop10
- The attacker could also use a zero day exploit which would be the worst case scenario since it’s new, so it can’t be detected at the beginning.
- The attacker could also exploit hardware or human vulnerabilities.


# Installation:
After the initial exploit and compromising the system, creating a persistent backdoor is key since if he loses the connection, gets detected, the initial access is removed or patched he will lose access. To learn more about about persistence on Windows, go here: 
https://tryhackme.com/room/windowslocalpersistence

# Persistence can be achieved with:
- Installing a [[Web Shell]] on the webserver. 
- Installing a backdoor on the victim’s machine using Meterpreter to install a backdoor. It’s a Metasploit Framework payload which gives an interactive shell which the attacker can use to interact with the victim’s shell remotely.
- Creating or modifying Windows services. This technique is known as [T1543.003](https://attack.mitre.org/techniques/T1543/003/) on MITRE ATT&CK. They can be modified to execute malicious scrips or payloads regularly as part of persistence. They can use tools like [[sc.exe]], Reg (reg-editor) to modify service configurations and masquerade the malicious payload by using a service name that is known to be related to the OS or legitimate software.
- Adding an entry to the [[Run Keys]] for the malicious payload in the Registry or the Startup Folder. This means the payload will execute each time the user logs in. There is a startup folder location for individual user accounts and a system wide startup folder that’s checked no matter who logs in.
- The attacker can use [[Timestomping]] to avoid detection by a forensic investigator by also making the malware appear as part of a legitimate program. 


# Command & Control:
- The attacker uses [[C2 Beaconing]] so that C2 can remotely control and manipulate the victim. 

# Actions on Objections (Exfiltration):
- Now that the attacker has compromised the system, achieved persistence and has established a way of communicating with C2, the attacker can achieve their main objective. These objectives can be:
	- Collecting credentials from users.
	- Privilege escalation (like domain administrator access from a workstation by exploiting a misconfiguration)
	- Internal reconnaissance (f.e the attacker interacts with the internal software to find its vulnerabilities)
	- Lateral movement
	- Collecting and exfiltrating sensitive data
	- Deleting backups and shadow copies (MS’s tech that creates backup copies, snapshots of files and volumes)
	- Overwrite or corrupt data