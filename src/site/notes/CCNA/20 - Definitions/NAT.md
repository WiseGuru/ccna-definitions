---
{"dg-publish":true,"permalink":"/ccna/20-definitions/nat/","tags":["defs_ccna"]}
---

#### NAT
*Network Address Translation (NAT)* is a way to map multiple private IP addresses inside a local network to a public [[CCNA/20 - Definitions/IPv4\|IP address]] before transferring the information onto the internet.

1. Static NAT
	1. Permanent one-to-one mapping between a public and private [[CCNA/20 - Definitions/IPv4\|IP address]]
	2. Usually used for servers
2. Dynamic NAT
	1. Uses a pool of available public IP addresses which are given out as-needed, first-come-first-served
	2. Requests are dropped once the pool runs out
3. PAT
	1. Port Address Translation, also called Dynamic NAT with Overload, is a type of dynamic NAT that bands several local IP addresses to a singular public one using [[CCNA/20 - Definitions/21 - OSI Layers/Layer 4\|Layer 4]] ports
	2. It can use one or more public IP addresses
		1. The first public [[CCNA/20 - Definitions/IPv4\|IP address]] is assigned like normal in Dynamic NAT
		2. The last public [[CCNA/20 - Definitions/IPv4\|IP address]] is translated using port numbers

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
