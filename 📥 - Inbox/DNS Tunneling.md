---
ID: "20250712220453"
---
# Overview:
Used for C2 by abusing the [[DNS]] protocol to covertly transmit data between an infected device and C2. This works even when traditional communication channels like HTTP and HTTPS are blocked by firewalls.

The commands are encoded into DNS queries and responses which allows the malware to communicate with the C2. This is allowed by default on most networks.

It could send queries like `dGhpcyBpcyBhIHRlc3Q=.attacker-domain.com`, which is a command in base64. It then communicates with C2 through DNS is through Recursive DNS Resolution. It sends a request that goes through the victim’s resolver and reaches the attacker-controlled authoritative DNS server for the attacker’s domain. Once it receives the query, decodes the data, it may send it back a DNS response with encoded commands in a TXT record or other [[DNS Record Types]], including NULL. The infected device then extracts the command and runs it.

This goes beyond beaconing and command execution, it could also be used for data exfiltration.

This is harder to detect than other forms of C2 beaconing since it’s usually allowed through firewalls but DNS is also typically very noisy and rarely inspected in depth.

# Detection & Mitigations:
- Unusual DNS query patterns, particularly frequent queries to uncommon or random-looking domains.
- Large volumes of TXT record responses.
- Queries containing encoded data (base64 strings)
- DNS filtering and detection tools (Zeek, Suricata, commercial DNS firewalls)


MITRE Technique:
https://attack.mitre.org/techniques/T1071/004/

