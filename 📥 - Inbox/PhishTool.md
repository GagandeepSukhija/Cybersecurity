---
ID: "20250725194753"
---
Elevates the perception of phishing to a severe form of attack and provides a responsive means of email security. Has both Community and Enterprise editions.

Core Features:
- Email Analysis:
	- Retrieves metadata from phishing emails to provide analysis with relevant explanations and capabilities to follow the email’s actions, attachments and URLs to triage the situation.
- Heuristic Intelligence:
	- OSINT is baked in so analysts can stay ahead and understand what [[TTPs]] were used for defense evasion to socially engineer the target.
- Classification and Reporting:
	- These are done so analysts can take action quicky. Reports and be generated to provide forensic records that can be shared.

Enterprise Features Include:
- Manage user-reported phishing event.s
- Report phishing finds to users and keep them engaged in the process.
- Email stack integration with MS365 and Google Workspace.

Analysis Tab:
- Headers - Routine info of the email f.e. source and destination email addresses, origin IP and DNS addresses and timestamp.
- Received Lines - Details of the traversal process across SMPT servers for tracing.
- X-headers - Extension headers added by recipient mailbox for additional information about the email.
- Security - Details on the email security frameworks such as [[SPF]], [[DKIM]], [[DMARC]]
- Attachments - Lists any attachments found in the email.
- Message URLs - Any associated external URLs in the email.

Indicators can be flagged as malicious and then can be flagged as resolved by classifying the email and setting up flagged artefacts and setting the classification codes. The details then appear on the Resolution tab of the analysis of the email.