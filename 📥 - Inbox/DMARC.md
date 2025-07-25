---
ID: "20250725195655"
---
DMARC (Domain-based Message Authentication, Reporting and Conformance) - Tells mail servers what to do if an email fails SPF/DKIM checks. Sends reports to domain owners so they can monitor abuse attempts.
		- Receiver checks if message passes SPF/DKIM and the domain aligns. If it fails then the DMARC policy tells the receiver to:
			- None - Take no action, just report.
			- Quarantine - Put in spam/junk.
			- Reject - Drop the email.
			- v = dmarc version, p = policy, rua = where to send aggregate reports, aspf=s = strict alignment on spf.
	- ```_dmarc.example.com. IN TXT
	 "v=DMARC1; p=reject; rua=mailto:dmarc-reports@example.com; aspf=s"```