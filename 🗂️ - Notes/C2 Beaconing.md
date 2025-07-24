---
ID: "20250712202048"
---
Opening a [[C2]] channel through the malware to remotely control and manipulate the victim. The infected host will consistently communicate with the C2 server, hence the term beaconing.

The compromised endpoint would communicate with an external server setup by an attacker to establish the channel. Then the attacker would have full control over the victim’s machine. Up till recently, they used [[IRC]] for the channel.

The most common C2 channels used by adversaries now are:
- HTTP & HTTPS - ports 80 and 443 (blends malicious traffic with legit traffic to help the attacker evade firewalls)
- [[DNS]] - The infected machine makes constant DNS requests to the DNS server that belongs to an attacker, this is known as [[DNS Tunneling]].
- An attacker or another compromised host can be the owner of the C2 infrastructure.