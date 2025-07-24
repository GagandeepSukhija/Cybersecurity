---
ID: "20250711124755"
---
A Record:
Resolve to IPv4 addresses.

AAAA Record:
Resolve to IPv6 addresses.

CNAME Record:
Resolve to another domain name, f.e. “TryHackMe's online shop has the subdomain name [store.tryhackme.com](http://store.tryhackme.com) which returns a CNAME record [shops.shopify.com](http://shops.shopify.com). Another DNS request would then be made to [shops.shopify.com](http://shops.shopify.com) to work out the IP address.”

MX (Mail Exchange) Record:
Resolve to the address of the servers that handle the email for the domain you’re querying. These records also come with a priority flag which tells the client in which order to try the servers. This is good for if the main server goes down and email needs to be sent to a backup server. It tries the lowest number first and then moves higher up if it fails. 

TXT Record:
Free text fields where any text-based data can be stored. These have multiple uses. Common ones include:
- List servers that have the authority to send an email on behalf of the domain (helps battle against spam and spoofed email)
- To verify ownership of the domain name when signing up for 3rd party services.
- Uses a few standardised formats for different uses:
	- SPF (Sender Policy Framework) - Checks if your domain is authorised to send email so it looks up your domain’s TXT records.
		- ```example.com.  IN  TXT  "v=spf1 include:_spf.google.com ~all"```
	- DKIM (Domain Keys Identified Mail) - Adds a digital signature to outgoing email headers so the receiver can verify the sender’s identity and check for tampering. It’s signed with a private key and then the receiver looks up your public key in your DNS TXT record to verify the signature.
		- ```selector1._domainkey.example.com. IN TXT
		 "v=DKIM1; k=rsa; p=MIGfMA0GCSqGSIb3DQEBA... (public key)"```
	- DMARC (Domain-based Message Authentication, Reporting and Conformance) - Tells mail servers what to do if an email fails SPF/DKIM checks. Sends reports to domain owners so they can monitor abuse attempts.
		- Receiver checks if message passes SPF/DKIM and the domain aligns. If it fails then the DMARC policy tells the receiver to:
			- None - Take no action, just report.
			- Quarantine - Put in spam/junk.
			- Reject - Drop the email.
			- v = dmarc version, p = policy, rua = where to send aggregate reports, aspf=s = strict alignment on spf.
	- ```_dmarc.example.com. IN TXT
	 "v=DMARC1; p=reject; rua=mailto:dmarc-reports@example.com; aspf=s"```


	- Domain Verification - A 3rd party such as a cloud service provider, email provider or search engine asks to prove ownership of your domain and it asks to add a DNS TXT record to the domain and the service checks it’s there.


Google’s Message Header Analyser:
https://toolbox.googleapps.com/apps/messageheader/
https://mxtoolbox.com/EmailHeaders.aspx
https://dkimvalidator.com/






