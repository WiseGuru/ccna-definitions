---
{"dg-publish":true,"permalink":"/ccna/20-definitions/ndp/","tags":["defs_ccna"],"created":"2023-11-05T10:55:11.000-08:00","updated":"2023-11-07T09:27:28.000-08:00"}
---

#### NDP
- *Neighbor Discovery Protocol (NDP)* is an [[CCNA/20 - Definitions/IPv6\|IPv6]] protocol that functions similarly to [[CCNA/20 - Definitions/ARP\|ARP]].
- It uses 5 [[CCNA/20 - Definitions/ICMP\|ICMPv6]] packets for router solicitation and neighbor discovery
	- *Router Solicitation* (*Type 133*)
		- Hosts send *RS* messages when they first connect to a network to discover routers
	- *Router Advertisement* (*Type 134*)
		- Routers advertise their presence with *RA* messages periodically
		- *RA*s are also sent in response to *Router Solicitation* packets
	- *Neighbor Solicitation* (*Type 135*)
		- Used by nodes to determine the *link-layer* address of a neighbor
		- Also used to verify if a neighbor is still reachable
	- *Neighbor Advertisement* (*Type 136*)
		- Sent in response to *Neighbor Solicitation* packets with information
		- Also sent unsolicited to provide new information quickly
	- *Redirect* (*Type 137*)
		- Used by routers to redirect hosts to a better first-hop router



# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
