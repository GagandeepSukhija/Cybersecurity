---
ID: "20250710165203"
---
The Pyramid of Pain is a concept that was designed to indicate the difficulty faced by an adversary in succeeding if they're denied certain indicators/you have some information on them.

![[proxy-image.jpg]]

Hash Values:
Hashes that correspond to suspicious/malicious files. [[Hash Lookup Tools]] can be used to verify if a hash is malicious or not since they’ll correspond with known malware. However, as a threat hunter, using file hashes as the [[IOC]] can become difficult even if they’re bullet-proof since it’s really trivial for an attacker to change it by simply changing a single bit of the malware or payload.


IP Addresses:
Suspicious IP Addresses that have been flagged/blocked due to a reputation of malicious activity. A common defense tactic against these is to [[Block, Drop and Deny]] inbound IPs as part of your external firewall. However, this tactic isn’t bullet-proof as it’s trivial for an attacker to persist using a new public IP address. One such way an attacker could do this is by using [[Fast Flux]].


[[Domain Names]]:
Domains/sub/sub-sub domains flagged as suspicious/malicious. If these are detected and mitigated then it’s a little bit more of a pain for attackers as they usually have to purchase a domain, register it and then modify the records. However, many [[DNS]] providers have loose standards and provide APIs to make it even easier for the attacker to change the domain.


[[Host Artifacts]] - Registry keys/values which are known to be created by specific pieces of malware. Files & directories in certain places with certain names etc. If these are discovered by the blue team then the attacker will likely need to change his attack tools and methodologies, making them a bit more annoyed and frustrated.


Network Artifacts:
Malicious signatures like URL patterns, user-agent strings, embedded C2 information, distinctive HTTP User-Agent/SMTP mailer values etc. If you can detect these and respond to the threat then the attacker would need more time to go back and change their tactics/modify their tools. This gives you more time to respond and detect the upcoming threats or remediate existing ones. URI patterns followed by the HTTP Post requests are also an artifact as well as the [[User-Agent]] itself. These artifacts can be detected in Wireshark PCAPs. You can also explore IDS logging from a source like Snort. If these custom user-agent strings can be blocked then their attempt to compromise the network will become more annoying.


Tools - Tools they use. This mostly refers to the things they bring with them. The software they use are usually utilities to create malicious documents for spear phishing, backdoors to establish C2, password crackers and other host-based utils they may want to use post-compromise. If you can detect and mitigate these they will most likely give up or try and create a new tool for the same purpose. This would require money into building a new one (if they’re capable) or finding a tool that has the same potential. They might also get some training on how to be proficient at using a certain tool. These tools can be used to create macro documents “maldocs” for spearphishing attempts, backdoors to create C2, custom .exe and .dll files, payloads and password crackers.

Malware Samples:
https://bazaar.abuse.ch/
https://malshare.com/

Detection Rules:
https://tdm.socprime.com/

Fuzzy Hashing Program:
https://ssdeep-project.github.io/ssdeep/index.html


[[TTPs]]: 
The method they use to complete their mission. This utilises the whole MITRE ATT&CK Matrix, which covers all the steps taken by an attacker to achieve their goal. This starts from phishing attempts to persistence and data exfiltration. If a TTP is detected and responded to quickly, the adversaries will have almost no chance to fight back because you already know what they’re doing and what they’re going to do next. This allows you to find any infected systems quickly, disable the possibility of lateral movement etc. This would leave an attacker with only two options: go back and do more research and training, get new tools or reconfigure them. Or, give up and find another target. An example of this could be a [[Pass-the-Hash]] attack. For example, you could detect it using Windows Event Log Monitoring and then remediate it, find the compromised host and stop the lateral movement.


How is this useful?
- Helps measure the potential usefulness of your intel.
- Measures the difficulty of obtaining that intel.
- Indicates the higher you are, the more resources your adversaries have to expend.

>[!QUOTE]+ David Bianco
>the amount of pain you cause an adversary depends on the types of indicators you are able to make use of.

