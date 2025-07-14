---
ID: "20250714233549"
---
MITRE Tactic TA0010 - https://attack.mitre.org/tactics/TA0010/


Unified Kill Chain:
The attacker seeks to steal the data. This is packaged using encryption and compression methods to avoid any detection. The C2 channel and tunnel are now handy for this process.


Cyber Kill Chain Definition:
 Now that the attacker has compromised the system, achieved persistence and has established a way of communicating with C2, the attacker can achieve their main objective. These objectives can be:
	- Collecting credentials from users.
	- Privilege escalation (like domain administrator access from a workstation by exploiting a misconfiguration)
	- Internal reconnaissance (f.e the attacker interacts with the internal software to find its vulnerabilities)
	- Lateral movement
	- Collecting and exfiltrating sensitive data
	- Deleting backups and shadow copies (MS’s tech that creates backup copies, snapshots of files and volumes)
	- Overwrite or corrupt data