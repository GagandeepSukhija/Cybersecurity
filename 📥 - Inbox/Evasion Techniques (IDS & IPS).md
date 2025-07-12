---
ID: "20250710154135"
References: "[[IDS & IPS]]"
---
Fragmentation:
Breaks up the packets so it can't detect a signature.

Avoiding Defaults:
Uses different ports than is typical for that protocol, f.e. may not be able to detect a trojan.

Coordinated, Low-Bandwidth Attacks:
A scan is coordinated between multiple attackers, specific ports and hosts could be allocated too. Since the scan is from multiple sources it makes it difficult for an IDS to correlate the packets and understand a network scan is in progress.

Pattern Change Evasion:
Changing the attack architecture slightly to change the signature, detection can be avoided.