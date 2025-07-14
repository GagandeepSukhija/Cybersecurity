---
ID: "20250714224714"
---
# Overview:
Created by Paul Pol and published in 2017 (updated in 2022), it aims to _complement_ other [[Cyber Kill Chain]] frameworks such as Lockheed Martin’s [[MITRE ATT&CK]].

It’s benefits lie in the fact it is modern (therefore current, with MITRE released in 2013) and contains a lot of detail. It officially has 18 phases. It covers the entire attack, from reconnaissance, post-exploitation and even includes identifying an attacker’s motivation. It also highlights a more realistic attack scenario. Various stages re-occur, an example of this once an attacker obtains access, they start to do recon again so they can pivot to another system.
![[708e85cf63230b21bacee32bfbd6d311.png]]
# Phase 1 - In (Initial Foothold):
- The focus of this series of phases is for the attacker to gain access to a system or networked environment. The attacker will employ numerous tactics to investigate the system for potential vulns that could be exploited to gain a foothold. F.E. a common tactic is using recon against a system to discover potential attack vectors (f.e. apps and services).
- It also includes the attacker creating a form of persistence and it also accounts for the attacker using a combination of the tactics listed.
- ![[9f902ef203a9aacb47ee847d7b3051d6.png]]


### Phases:
-  [[Reconnaissance]] - TA0043:
	- https://attack.mitre.org/tactics/TA0043/
- [[Weaponisation]] - TA0001:
	- https://attack.mitre.org/tactics/TA0001/
- [[Social Engineering]] - TA001:
	- https://attack.mitre.org/tactics/TA0001/
- [[Execution]] - TA0002:
	- https://attack.mitre.org/tactics/TA0002/
- [[Persistence]] - TA0003:
	- https://attack.mitre.org/tactics/TA0003/
- [[Defence Evasion]] - TA0005:
	- https://attack.mitre.org/tactics/TA0005/
- Command & Control ([[C2]]) - TA0011:
	- https://attack.mitre.org/tactics/TA0011/
- [[Pivoting]] - TA0008:
	- https://attack.mitre.org/tactics/TA0008/


# Phase 2 - Through (Network Propagation):
This follows a successful foothold being established on the target network. The attacker would seek to gain additional access and privileges to systems and data to fulfill their goals. The attacker would setup a base on one of the systems to act as their pivot to use it to gather information about the internal network.

- [[Pivoting]] - TA0008:
	- https://attack.mitre.org/tactics/TA0008/
- [[Discovery]] - TA0007:
	- https://attack.mitre.org/tactics/TA0007/
- [[Privilege Escalation]] - TA0004:
	- https://attack.mitre.org/tactics/TA0004/
- [[Execution]] - TA0002:
	- https://attack.mitre.org/tactics/TA0002/
- [[Credential Access]] - TA0006:
	- https://attack.mitre.org/tactics/TA0006/
- [[Lateral Movement]] - TA0008:
	- https://attack.mitre.org/tactics/TA0008/


# Phase 3 - Out (Actions on Objectives):
“This phase wraps up the journey of an adversary’s attack on an environment, where they have critical asset access and can fulfil their attack goals. These goals are usually geared toward compromising the confidentiality, integrity and availability ([[CIA]] Triad).” - THM

- [[Collection]] - TA0009
	- https://attack.mitre.org/tactics/TA0009/
- [[Exfiltration]] - TA0010
	- https://attack.mitre.org/tactics/TA0010/
- [[Impact]] - TA0040:
	- https://attack.mitre.org/tactics/TA0040/
- Objectives:
	- With all the power and access needed, the attacker now seeks to achieve their strategic goal for the attack. This could be financial (ransomware for example), damaging reputation (releasing private and confidential info to public).

