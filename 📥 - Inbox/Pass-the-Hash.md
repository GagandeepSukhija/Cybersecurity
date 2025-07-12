---
ID: "20250711144157"
---
An attacker captures a password hash (not the plaintext), they can then use this for authentication and gain lateral access to other networked systems. This exploits the way authentication protocols work and it removes the need to decrypt the hash into a plain text password. Password hashes remain static for each session until the password is changed, they can be scraped using a system’s active memory and other techniques. 

On Windows, a password once created is hashed and stored in one of the following locations:
- The Security Accounts Manager (SAM)
- The Local Security Authority Subsystem (LSASS) process memory
- A Credential Manager (CredMan) store
- A ntds.dit database in Active Directory
- Elsewhere

To gain the hash to begin with, the attacker would need administrative access to lift the hash, once they’ve done so then they can move laterally relatively easily. This would also provide them with plenty of opportunity to escalate privileges too.

This can be countered by using the Principle of Least Privilege. Where only the least amount of privileges and permissions needed for each user is given to limit the opportunity to escalate. Rotating passwords frequently or after a known compromise can reduce the window of time a compromised hash could be used. OTPs are also great for this.