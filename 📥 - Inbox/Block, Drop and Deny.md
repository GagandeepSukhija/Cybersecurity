---
ID: "20250710211401"
---
Firewall rules that dictate how it responds to packets received.

Drop:
- Discards the packet silently.
- It doesn’t notify the sender.
- This works to vanish from attackers’ scans.
- This is good for stealth and rate-limiting scans (because they won’t get a response and therefore are less likely to persist with their scans).

Deny:
- Rejects the packet and sends a response back.
- ICMP “Destination Unreachable” for IP
- TCP RST for TCP connections 
	- RST = RESET, a special response packet for TCP. Terminates the connection immediately. Says the port is closed so it’s a clear and fast signal.
- This is if you want the sender to know the connection is explicitly blocked.
- Good for internal systems, lets users know they’re not authorised.

Block:
- This isn’t a technical rule, this is just a general term used in some tools which usually means DROP or DENY.