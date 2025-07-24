---
ID: "20250711140009"
---
A HTTP method used to receive data from a server. This could be asking for a webpage.

GET requests contain the data location (sent in the URL/query string), they are visible in logs (of web servers and proxies), they can be cached by browsers or CDNs, Idempotent (meaning that if repeated it shouldn’t change anything on the server). GET requests aren’t designed for sensitive data so passwords, tokens, PII should never be sent via GET.

Attackers often use GET requests for recon and enumeration to discover pages like /admin, /login etc. 

SQLi/XSS Attacks - The payloads often appear in GET parameters.
`?search=<script>alert(1)</script>`

Poorly designed apps can leak tokens in URLs which will then show in logs or referrer headers.

Phishing links use malicious GET URLs that redirect to fake login pages or inject code.

