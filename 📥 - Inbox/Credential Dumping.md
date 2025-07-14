---
ID: "20250715000530"
---
Post exploitation technique to extract usernames, passwords, password hashes or authentication tokens from a compromised system.

They can target specific locations in memory/files where they’re stored:
- [[LSASS]] - The most common target. Credentials in memory for currently logged in users.
- [[SAM]]
- [[NTDS.dit]]