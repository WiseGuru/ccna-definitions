---
{"dg-publish":true,"permalink":"/ccna/20-definitions/tkip/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-13T08:10:57.000-08:00"}
---

#### TKIP
1. *TKIP* (Temporal Key Integrity Protocol) is backwards compatible with [[CCNA/20 - Definitions/WEP\|WEP]]
	1. Built as a stop-gap for WEP
		1. Based on WEP to enhance security of existing hardware
	2. Add various security features
		1. *[[CCNA/20 - Definitions/MIC\|MIC]] (Message Integrity Check)* is added to protect integrity of messages
			1. Includes the sender's MAC address to ensure sender's identity
			2. a Timestamp is added to the MIC to prevent [[CCNA/20 - Definitions/replay attacks\|replay attacks]]
		2. a *Key Mixing Algorithm* creates a unique WEP key for each frame
		3. The *Initialization Vector* is doubled from 24-bits to 48-bits


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-1-11 
### Contributors

### Sources
