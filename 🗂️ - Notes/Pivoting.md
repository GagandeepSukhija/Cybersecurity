---
ID: "20250714234209"
---
MITRE Tactic TA0008 - https://attack.mitre.org/tactics/TA0008/

This is different to Lateral Movement as it doesn’t use the same compromised credentials, instead, the attacker uses the compromised system as a proxy to jump to another one in the network that aren’t otherwise reachable (they’re not exposed to the internet). There are often many devices that fit this criteria within an organisation that aren’t directly reachable. An example of this is a compromised web server that is publicly accessible to attack other systems within the same network that aren’t accessible via internet.