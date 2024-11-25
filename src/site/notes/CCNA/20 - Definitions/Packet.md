---
{"dg-publish":true,"permalink":"/ccna/20-definitions/packet/","tags":["defs_ccna"]}
---

#### Packet
- An *IP Packet* is the data unit sent at the [[CCNA/15 - OSI Layers/Layer 3\|Network layer]]. 



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/i-pv4-packet-header/#i-pv4-header" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




An *[[CCNA/20 - Definitions/IPv4\|IPv4]] packet header*, depending on the options selected, can range in size from **160 bits (20 bytes)** and **480 bits (60 bytes)**
- *Version*
	- 4 bits
	- Always set to 4 (0100)
- *IHL* (Internet Header Length)
	- 4 bits
	- Specifies the number 32-bit words
		- 5 words end at the destination IP address
		- 6 or more mean that there are Options configured
- *[[CCNA/20 - Definitions/DSCP\|DSCP]]* (Differentiated Services Code Point)
	- 6 bits
	- Identifies the kind of service the pack contains, and what priority it should receive, and how likely it is to be dropped during network congestion
- *ECN* (Explicit Congestion Notification)
	- 2 bits
- *Total Length*
	- 16 bits
- *Identification*
	- 16 bits
- *Flags*
	- 3 bits
- *Fragment Offset*
	- 13 bits
- *Time To Live*
	- 8 bits
	- Used to prevent routing loops
	- Indicates hop count, which each router decrementing the value by 1
- *Protocol*
	- 8 bits
	- Indicates the IP Protocol, per an assigned [[CCNA/20 - Definitions/IANA\|IANA]] protocol number
	- [List of IP protocol numbers - Wikipedia](https://en.wikipedia.org/wiki/List_of_IP_protocol_numbers)
- *Header Checksum*
	- 16 bits
- *Source IP Address*
	- 32 bits
- *Destination IP Address*
	- 42 bits
- *Options (if IHL is greater than 5)*
	- Up to 320 bits long

![IP-header-2.png](/img/user/CCNA/Attachments/IP-header-2.png)
Source: [Internet Protocol version 4 - Wikipedia](https://en.wikipedia.org/wiki/Internet_Protocol_version_4#Header)




# Metadata
### OSI or TCP/IP Layer
[[CCNA/15 - OSI Layers/Layer 3\|Layer 3]]
### CCNA Exam Topic

### Contributors

### Sources
[Internet Protocol version 4 - Wikipedia](https://en.wikipedia.org/wiki/Internet_Protocol_version_4)


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/i-pv6-packet-header/#i-pv6-header" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### IPv6 Header
**320 bits** in total (**40 bytes**)
- Version: 4 bits
	- Always 6 (0110)
- Traffic class: 6+2 bits
	- QoS Markings
- Flow Label: 20 bits
	- Used to identify specific traffic flow
- Payload length: 16 bits
	- Length of the encapsulated [[CCNA/15 - OSI Layers/Layer 4\|Layer 4]] segment
- Next Header: 8 bits
	- Indicates the encapsulated [[CCNA/15 - OSI Layers/Layer 4\|Layer 4]] protocol
- Hop Limit: 8 bits
	- Functions like the IPv4 [[CCNA/20 - Definitions/TTL\|TTL]] field
- Source Address: 128 bits
- Destination address: 128 bits
![IPv6-Packet-header-1.png](/img/user/CCNA/Attachments/IPv6-Packet-header-1.png)
Source: [IPv6 packet - Wikipedia](https://en.wikipedia.org/wiki/IPv6_packet#Fixed_header)





</div></div>







# Metadata
### OSI or TCP/IP Layer
[[CCNA/15 - OSI Layers/Layer 3\|Layer 3]]

### CCNA Exam Topic

### Contributors

### Sources
[Internet Protocol version 4 - Wikipedia](https://en.wikipedia.org/wiki/Internet_Protocol_version_4)
[IPv6 packet - Wikipedia](https://en.wikipedia.org/wiki/IPv6_packet)