---
ID: "20250710160645"
---
Tactics, Techniques & Procedures.

Identifying these during an incident can help establish potential attribution and attack framework. 

An Example:
The target of an attempted attack receives a hostile email attachment containing a zero-day exploit and payload to install a new, unknown malware. This attack is performed by a nation-state group which has consistently targeted U.S. Department of Defense using similar TTPs.

Benefits:
- They help to identify a common vector of attack.
- They help establish persistent threat actors such as nation-states.
	- By helping provide attribution, command and control infrastructure (C2) can also be identified which is extremely valuable.
	- Traces of data from that C2 can then be detected and analysed whereas before they might have been missed.
	- Likely vectors and payloads can also be identified easier.


Post Incident TTPs:
- Help to boost strategic research and response.
- Shows lessons learned, additional research into the campaign, related attack data.
- Matures the TTP and allows implementation of more proactive measures and controls for future attacks with those TTPs. F.e. some threat actors use the same payloads.
- Understanding TTPs of a particular threat actor helps to harden against those specific threats.

R&D & Threat Actor Communities:
- Threat actors conduct recon before attacking but it's not reported often as it's harder to detect. R&D and threat actor communities can reveal other TTPs of interest.
- By doing R&D and scouring these communities you can find other associated threat actors on forums etc.
- Identify the tools used by seeing what is shared and sold.
- By learning how these tools work, you can alter your policies to flag them sooner/prevent them entirely.

For best use - TTPs should be stored in a way that is accessible and usable by all but if it's an SME then it makes more sense to have this outsourced or focused on just a few that you commonly face and standard eCrime attacks.

For More Information:
https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-200a