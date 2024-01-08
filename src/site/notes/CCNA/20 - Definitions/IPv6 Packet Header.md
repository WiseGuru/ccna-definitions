---
{"dg-publish":true,"permalink":"/ccna/20-definitions/i-pv6-packet-header/","tags":["defs_ccna"],"created":"2023-11-05T10:55:11.000-08:00","updated":"2023-11-08T14:42:44.000-08:00"}
---

#### IPv6 Header
**320 bits** in total (**40 bytes**)
- Version: 4 bits
	- Always 6 (0110)
- Traffic class: 6+2 bits
	- QoS Markings
- Flow Label: 20 bits
	- Used to identify specific traffic flow
- Payload length: 16 bits
	- Length of the encapsulated [[CCNA/20 - Definitions/21 - OSI Layers/Layer 4\|Layer 4]] segment
- Next Header: 8 bits
	- Indicates the encapsulated [[CCNA/20 - Definitions/21 - OSI Layers/Layer 4\|Layer 4]] protocol
- Hop Limit: 8 bits
	- Functions like the IPv4 [[CCNA/20 - Definitions/TTL\|TTL]] field
- Source Address: 128 bits
- Destination address: 128 bits
![IPv6-Packet-header-1.png](/img/user/Attachments/IPv6-Packet-header-1.png)
Source: [IPv6 packet - Wikipedia](https://en.wikipedia.org/wiki/IPv6_packet#Fixed_header)




# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
[IPv6 packet - Wikipedia](https://en.wikipedia.org/wiki/IPv6_packet)