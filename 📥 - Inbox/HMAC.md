---
ID: "20250710183227"
---
Hash-Based Message Authentication Code:
A cryptographic algorithm that's used to verify the integrity and authenticity of a message. It's used widely in secure communication. Examples include: APIs, TLS and network protocols.

The essence of HMAC is using a secret key and a secure hashing algorithm like SHA256 or ALS and using the original message to output a fixed-length digest. This digest is the HMAC. This is then used to send the message _and_ the HMAC to verify authenticity and integrity.

This can then be compared on both ends of communication by using the same secret key and comparing the digest. 

This means that even if an outsider was to know the original message and the hashing algorithm, they couldn't fake authenticity since they wouldn't have the secret key.

So, HMAC is designed to be a tamper-proof signature created using a secret key and a message.



The Formula:
```
HMAC(K, m) = H((K ⊕ opad) ∥ H((K ⊕ ipad) ∥ m))
```

Where:
- `H` = hash function (e.g. SHA-256)
- `K` = secret key (if longer than the block size, it’s hashed first)
- `m` = message
- `⊕` = bitwise XOR
- `∥` = concatenate
- `ipad` = inner pad (0x36 repeated)
- `opad` = outer pad (0x5C repeated)

Let’s say:
- Hash function: SHA-256 (output: 32 bytes)
- Block size of SHA-256: 64 bytes

 Step 1 - Key Preprocessing
- If `K` is longer than 64 bytes, it's hashed to shorten it.
- If shorter, it's padded with 0x00 bytes to reach 64 bytes.

Step 2 - Define Inner and Outer Pads
- `ipad` = 64 bytes of `0x36`
- `opad` = 64 bytes of `0x5C`

Step 3 - Compute Inner Hash:
```inner = H((K ⊕ ipad) ∥ message)```

Step 4 - Compute Final HMAC:
```HMAC = H((K ⊕ opad) ∥ inner)```

To summarise:
HMAC is the summation of the hash of the secret key with a bitwise XOR of the inner pad concatenated with the message. Then the same for the outer pad but concatenated with the hash of the inner.

The ipad and opad values are universal for the HMAC algorithm. These values are 0x36 and 0x5c respectively.