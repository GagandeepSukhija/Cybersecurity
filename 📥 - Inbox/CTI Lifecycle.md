---
ID: "20250724123346"
---
![[Pasted image 20250724123400.png]]

Threat intel is obtained by transforming raw data into contextualised, action oriented insights. This is used to triaging incidents. 

This cycle has 6 phases:

Direction:
- Every threat intel program requires defined objectives and goals. This involves identifying the following:
	- Information assets & business processes that need defending.
	- Potential impact of losing assets/process interruptions.
	- Sources of data/intel to be used towards protection.
	- Tools & resources needed to defend assets.

Collection:
- Security Analysts collect the data needed. This is done via commercial and open source resources. Since there’s such a high volume of data that analysts face, it’s recommended to automate this phase so that more time can be spent triaging incidents.

Processing:
- Raw logs, vuln information, malware, network traffic. These usually come in different formats and need to be sanitised and organised, assigned tags and presented visually in an understandable format for analysts. [[SIEMs]] are used for this to allow for quick parsing of data.

Analysis:
- Data has been collected and processed so now it must be analysed for insights to make informed decisions. These could be:
	- Investigating threats by uncovering indicators and attack patterns.
	- Defining an action plan to avert an attack and defend infrastructure.
	- Strengthening security controls or justifying investment for additional resources.

Dissemination:
- Different types of stakeholders consume the intelligence in different languages and formats. F.e. C-suite members need a concise overview that covers adversary trends, financial implications and strategic recommendations. Analysts inform the technical team about [[IOC]]s, adversary [[TTPs]] and action plans.

Feedback:
- Using responses from stakeholders to improve threat intel process and implementation of security controls. Feedback has to be a regular interaction between the teams to keep the lifecycle working.
