---
ID: "20250725195634"
---
DKIM (Domain Keys Identified Mail) - Adds a digital signature to outgoing email headers so the receiver can verify the sender’s identity and check for tampering. It’s signed with a private key and then the receiver looks up your public key in your DNS TXT record to verify the signature.
		- ```selector1._domainkey.example.com. IN TXT
		 "v=DKIM1; k=rsa; p=MIGfMA0GCSqGSIb3DQEBA... (public key)"```