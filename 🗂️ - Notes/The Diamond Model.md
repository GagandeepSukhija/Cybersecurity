---
ID: "20250715031654"
---
“**The Diamond Model of Intrusion Analysis** was developed by cybersecurity professionals - Sergio Caltagirone, Andrew Pendergast, and Christopher Betz in 2013.” - THM

Useful to communicate a breach/intrusion to people who are non-technical whether they are executives or stakeholders.

Composed of 4 core features:
- [[Adversary]]
- [[Infrastructure]]
- [[Capability]]
- [[Victim]]

It established the “fundamental atomic element of any intrusion activity”. It also contains 2 additional axes: Social, Political and Technology. 

It contains the essential concepts of intrusion analysis and adversary operations but is still flexible to encompass new ideas and concepts. It also contains opportunities to integrate real-time intelligence for network defence, automating correlation across events, classifying events with confidence into adversary campaigns and forecasting adversary operations while planning and gaming mitigation strategies.

The Diamond Model is useful because it helps you identify the elements of an intrusion but also helps you to explain to non-technical people about what happened during an event or any valuable information about the malicious threat actor.

There are 6 possible meta-features that can be added to the mode, these are optional but they can add some valuable information and intelligence to the model.

These are:
- Timestamps - date and time of the events.
- Phase - [[Unified Kill Chain]], [[Cyber Kill Chain]]
- Results - These aren’t always known or you may not have high confidence in a conclusion but it’s important to capture the post-conditions of the event such as info gathered from the recon stage, successful passwords, data exfiltration but just the post-conditions in general. The event’s results can be labelled as success/failure/unknown and can be related to the [[CIA]] triad.
- Direction - “This meta-feature helps describe host-based and network-based events and represents the direction of the intrusion attack. The Diamond Model of Intrusion Analysis defines seven potential values for this meta-feature: Victim-to-Infrastructure, Infrastructure-to-Victim, Infrastructure-to-Infrastructure, Adversary-to-Infrastructure, Infrastructure-to-Adversary, Bidirectional or Unknown.” - THM
- Methodology - Allows the analyst to describe the general class of the intrusion f.e. phishing, DDoS, breach, port scan etc.
- Resources - Every intrusion needs one or more external resources to be satisfied to succeed. F.e. software (OS, virtualisation software, Metasploit framework), knowledge (how to use Metasploit), information (credentials to masquerade), hardware (servers, workstations, routers), funds (money to purchase domains), facilities (electricity or shelter), access (network path from the source host to the victim and vice versa, network access from an ISP).

The Social-Political Axioms:
- The needs and intent of the adversary. This could be financial gain, gaining acceptance/reputation int he hacker community, hacktivism, espionage.

Technology:
Highlights the relationship between the core features: capability and infrastructure. Capability and Infrastructure describe how the adversary operates and communicates.

