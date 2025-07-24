---
ID: "20250712022843"
---
The USB dongle was packaged with Best Buy branding, claiming to have a redeemable gift card inside. It contained an official looking letter with Best Buy’s logo and other branding elements which said they received a $50 gift card for being a regular customer. “You can spend it on any product from the list of items presented on an USB stick,” the letter read. It was never plugged into any computer as the person who received it had security training and was passed along for analysis.

The dongle model was traced to a Taiwanese website where it was being sold for the equivalent of $7 with the name “BadUSB Leonardo USB ATMEGA32U4”.

In 2014 at Black Hat, a team of researchers from Security Research Labs in Berlin showed that USB firmware could be reprogrammed to identify as a keyboard and can be used to send commands to deploy malware. The USB contained an Arduino ATMEGA32U4.

The USB would execute an obfuscated PowerShell script which then reaches out to a domain set up by the attackers and downloads a secondary PowerShell payload. This then deploys a third, JavaScript-based payload which is executed through [[WSH]].

The 3rd payload generates a UID for the computer and registers it to a remote C2 server. It then receives additional JavaScript code from the server. The goal of this 4th payload is to gather information on the system, for example: the user’s privilege, domain name, time zone, language, OS, hardware information, list of running processes, whether MS Office and Adobe Acrobat are installed and more.

Once this is done, the script enters a loop and periodically checks with the C2 to see if there are new commands to execute.

Security Researchers from Kaspersky Lab, Costin Raiu and Michael Yip commented on Twitter that the malware used and infrastructure match that used by the [[FIN7]] gang.
https://twitter.com/craiu/status/1243167791483686913

The malware, GRIFFON and infrastructure match FIN7, it’s the first time that Raiu has seen them use a physical USB attack vector. He estimates the campaign dates back to at least December 2019. This can be seen from submissions on VirusTotal. FireEye Intelligence has also been tracking them and found them sending USPS packages to US based organisations with the same thing, with a GRIFFON backdoor in the USB.

The FBI sent a private alert to companies on Thursday confirming that FIN7 was behind these attacks. 

This type of attack would be a lot more malicious when more employees are working remotely since there are no security staff to intercept them before they’re used or one of their family members might use it before they have a chance to stop it.

# Reference:
https://www.csoonline.com/article/569163/cybercriminal-group-mails-malicious-usb-dongles-to-targeted-companies.html