---
ID: "20250710185401"
---
Indicators of Compromise:
Anything that you can detect that may suggest a breach, attack or compromise.
These are clues that you can find in logs, network traffic or files that point to malicious activity.

Some Examples:
IP Addresses
Domain Names
File Hashes
Registry Keys
Process Names
Log Patterns
Email Artifacts


IOCs are used in IDSs, IPSs and SIEMs to quickly detect threats.

An example of this may be an IP that’s on your IOC watchlist as it’s associated with C2 activity which is found in your logs in Splunk. Now it’s been caught you can quickly investigate the host and isolate it. So the IP was the IOC.