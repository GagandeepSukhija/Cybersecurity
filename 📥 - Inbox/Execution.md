---
ID: "20250714232037"
---
MITRE Tactic TA0002 - https://attack.mitre.org/tactics/TA0002/

This is where malicious code is _deployed_. 

Following this scenario of a Maldoc attack using MS Office applications, the attacker sends 2 emails, one with a phishing link to a face 365 login page and another with a macro attachment that’ll execute ransomware. The attacker obtains 2 victims.
- Once he’s gained access, they can exploit software, the system, exploit server-based vulnerabilities to escalate privileges or use [[Lateral Movement]].
- To learn about server/web-based vulnerabilities, go to the following:
	- https://tryhackme.com/room/owasptop10
- The attacker could also use a zero day exploit which would be the worst case scenario since it’s new, so it can’t be detected at the beginning.
- The attacker could also exploit hardware or human vulnerabilities.

The UKC describes this as:
- An attacker exploiting weaknesses/vulns present in a system to perform code execution Examples are:
	- Uploading/executing a reverse shell to a web app.
	- Interfering with an automated script on the system to execute code.
	- Abusing a web-app vulnerability to execute code on the system its running on.


During the 2nd phase of the [[Unified Kill Chain]], after gaining initial access the attacker uses the pivot system as their host. “Remote trojans, C2 scripts, malicious links and scheduled tasks are deployed and created to facilitate a recurring presence on the system and uphold their persistence.” - THM

