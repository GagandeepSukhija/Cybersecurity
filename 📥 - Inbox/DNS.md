---
ID: "20250711122555"
---
Domain Name Systems.
Instead of having to remember every IP address, you can use the website name instead of the IP address since the DNS will translate it.

[[Domain Hierarchy]]

[[DNS Record Types]]

What happens when a DNS Request is made:
- The computer first checks its local cache to see if you’ve looked it up recently and if not, it requests your Recursive DNS Server.
- The Recursive DNS server is usually provided by your ISP. You can also choose your own. This also has a local cache for recently searched domain names and if found it’ll be sent to your computer. If it can’t be found then it begins by querying the internet’s root DNS servers.
- The root server will refer you to the correct TLD.
- The TLD server holds records for where to find the authoritative server to answer the request. The authoritative server is also known as a nameserver. For example, Cloudflare. It’s common to find multiple nameservers for a domain name to act as a backup in case one goes down.
- An authoritative server is responsible for storing the DNS records for a particular domain name and where any updates to your domain name DNS records would be made. DNS records come with a TTL (seconds), this value dictates how long the response should be saved locally until you have to look it up again.


![[5f04259cf9bf5b57aed2c476-1724075620083.png]]