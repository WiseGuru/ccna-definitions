---
{"dg-publish":true,"dg-path":"20 - Definitions/Loopback interface.md","permalink":"/20-definitions/loopback-interface/","tags":["defs_ccna"]}
---

#### Loopback Interface
- A *Loopback Interface* is a virtual interface on a network device that is used to communicate with itself.
	- Primarily used for diagnostics and troubleshooting to ensure other processes and protocols are working.
	- Often they are used on networking devices to ensure there is an *IP address* that is *unique* to that device, and *not dependent* on an *active link*, for management purposes
	- In [[CCNA/20 - Definitions/Dynamic Routing Protocols\|Dynamic Routing Protocols]] like [[CCNA/20 - Definitions/OSPF\|OSPF]], it can be used when deciding router priority or identification
- Example addresses are often 1.1.1.1, 2.2.2.2, etc., but [these are real addresses on the internet and should not be used](https://www.cloudflare.com/learning/dns/what-is-1.1.1.1/)
	- A better example might be 10.255.0.1, 10.255.0.2, etc.
- This is not the same as [[CCNA/20 - Definitions/IPv4 Address Classes\|Loopback addresses]], which are defined in *RFC 1918* with the range 127.0.0.0/8, reserved block from [[CCNA/20 - Definitions/IPv4 Address Classes\|Class A]]


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
