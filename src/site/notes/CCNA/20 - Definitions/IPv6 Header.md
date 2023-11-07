---
{"dg-publish":true,"permalink":"/ccna/20-definitions/i-pv6-header/","tags":["defs_ccna"]}
---

#### IPv6 Header
- 320 bits in total (40 bytes)
- ![IPv6 Header-1.png|700](/img/user/Attachments/IPv6%20Header-1.png)
	- Version: 4 bits
		- Always 6 (0110)
	- Traffic class: 6+2 bits
		- QoS Markings
	- Flow Label: 20 bits
		- Used to identify specific traffic flow
	- Payload length: 16 bits
		- Length of the encapsulated Layer 4 segment
	- Next Header: 8 bits
		- Indicates the encapsulated Layer 4 protocol
	- Hop Limit: 8 bits
		- Functions like the IPv4 TTL field
	- Source Address: 128 bits
	- Destination address: 128 bits





# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
[IPv6 packet - Wikipedia](https://en.wikipedia.org/wiki/IPv6_packet#Fixed_header)