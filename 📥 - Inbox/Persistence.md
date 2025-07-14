---
ID: "20250714232624"
---
MITRE Tactic TA0003 - https://attack.mitre.org/tactics/TA0003/

After the initial exploit and compromising the system, creating a persistent backdoor is key since if he loses the connection, gets detected, the initial access is removed or patched he will lose access. To learn more about about persistence on Windows, go here: 
https://tryhackme.com/room/windowslocalpersistence

# Persistence can be achieved with:
- Installing a [[Web Shell]] on the webserver. 
- Installing a backdoor on the victim’s machine using Meterpreter to install a backdoor. It’s a Metasploit Framework payload which gives an interactive shell which the attacker can use to interact with the victim’s shell remotely.
- Creating or modifying Windows services. This technique is known as [T1543.003](https://attack.mitre.org/techniques/T1543/003/) on MITRE ATT&CK. They can be modified to execute malicious scrips or payloads regularly as part of persistence. They can use tools like [[sc.exe]], Reg (reg-editor) to modify service configurations and masquerade the malicious payload by using a service name that is known to be related to the OS or legitimate software.
- Adding an entry to the [[Run Keys]] for the malicious payload in the Registry or the Startup Folder. This means the payload will execute each time the user logs in. There is a startup folder location for individual user accounts and a system wide startup folder that’s checked no matter who logs in.
- The attacker can use [[Timestomping]] to avoid detection by a forensic investigator by also making the malware appear as part of a legitimate program. 

In the UKC:
- Techniques used to maintain access to a system they’ve gained a foothold on. Examples:
	- Creating a service on the system allowing the attacker to regain access.
	- Adding the target system to a [[C2]].
	- Leaving other forms of backdoors that execute when certain actions occur (F.e. a reverse shell will execute when a sysadmin logs in).