---
ID: "20250711132603"
---
Jamf - “Punycode is a way of converting words that cannot be written in ASCII, into a Unicode ASCII encoding.”

[[DNS]] was designed in the 1980s and only supports ASCII. But the modern web needs to support internationalised domain names (IDNs) (accented characters, cyrillic etc.). Punycode converts Unicode into ASCII to solve this issue.

For Example:
`müller.de`|`xn--mller-kva.de`
`пример.рф`|`xn--e1afmkfd.xn--p1ai`
`español.com`|`xn--espaol-zwa.com`

It always starts with xn– to indicate that it’s Punycode.

Punycode can be used to phish victims with similar looking characters, however, browsers have become better at showing their ASCII form in the address bar now.