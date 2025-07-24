---
ID: "20250710212458"
---
A [[DNS]] technique used by botnets to hide phishing, web proxying, malware delivery and malware communication activities behind compromised hosts acting as proxies. The purpose of using the network is to make the communication between malware and its C2 server challenging to be discovered by security professionals.

The main concept is it has multiple IP addresses associated with a domain name, which also constantly changes. The goal of Fast Flux networks is to maintain uptime so they avoid losses to their revenue streams. This is the same as benign service providers who build redundancy in their systems to ensure uptime.

One such technique that is used is Round Robin in the DNS (RRDNS) or for their Content Delivery Networks (CDN).

The A record for the domain holds the address for the server used, so once a group of compromised machines is acquired, the A record must change so he can rapidly change switch them. A simple script can be used to automatically update the hosts for where the DNS records of the site point. The Time To Live (TTL), is set quite low to ensure that earlier DNS responses aren’t cached for long.

![[word-image-3.png]]

However, this can be taken down by taking the DNS server itself down. But this can be fixed by moving the DNS resolution itself to a fast flux network. 

This is how normal [[DNS Resolution]] works:

By using a fast flux network to replace the previous name server. This is called [[Double Flux]].