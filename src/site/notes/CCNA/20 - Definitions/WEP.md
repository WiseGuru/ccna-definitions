---
{"dg-publish":true,"permalink":"/ccna/20-definitions/wep/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-07T17:02:03.411-08:00"}
---

#### WEP
- *Wire-Equivalent Privacy (WEP)* encrypts traffic with [[CCNA/20 - Definitions/RC4\|RC4]] Symmetric streaming encryption
- Uses a shared key, which is combined with a "**24-bit Initialization Vector**" to make the final encryption key 64 or 128 bits long
- NOT SECURE
	- The *24-bit IV* is limited to 16.7 million values (2^24), which can easily be repeated on a busy network
		- Compare to [[CCNA/20 - Definitions/AES\|AES]] minimum encryption key length of 128 bits, with 340 tredecillion values (2^128)
	- WEP implementations often reused *IVs*, which made it easier to predict and decrypt
- [[CCNA/20 - Definitions/TKIP\|TKIP]] was implemented as a stop-gap for WEP
	- It doubled the *IV* from 24 to 48 bits as a stop-gap
	- It used a *Key Mixing Algorithm* to create unique WEP keys for each frame







# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
