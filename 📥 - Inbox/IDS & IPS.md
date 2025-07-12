---
ID: "20250710153400"
---
Intrusion Detection Systems - Detect intrusions using policies and monitoring for malicious activity. This is reported to the SIEM.

Intrusion Prevention Systems - The same as an IDS, except these can also respond independently on discovery.

Signature Based - Detects threats using unique patterns such as byte sequences in network traffic or sequences in malware. This works but it cannot detect new attacks because no signature would be available.

Anomaly Based - Uses ML to create a model of trustworthy activity and then compares behaviour to that model. If it doesn't line up then it flags it as malicious. Though this works better, it can flag a lot of false positives.