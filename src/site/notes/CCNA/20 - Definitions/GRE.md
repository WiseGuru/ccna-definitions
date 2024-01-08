---
{"dg-publish":true,"permalink":"/ccna/20-definitions/gre/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-08T13:58:01.000-08:00"}
---

#### GRE
- *Generic Routing Encapsulation* creates *unencrypted tunnels* between two clients
- It does not encrypt traffic in transit, but it's able to encapsulate many [[CCNA/20 - Definitions/21 - OSI Layers/Layer 3\|Layer 3]] protocols like *multicast* and *broadcast* messages
	- Because of this, it is often used in conjunction with [[CCNA/20 - Definitions/IPsec\|IPsec]], which encrypts traffic, but is unable to encapsulate many *Layer 3* protocols.
- *GRE over IPsec* is typically managed by *routers* and not *end hosts*
	- A host's packet is *encapsulated* in *GRE*, and then *encrypted* and sent over an *IPsec tunnel*
	- (compared to [[Remote Access VPNs\|Remote Access VPNs]])

#### GRE over IPsec
Example: **HostA** is sending a packet over the WAN to **HostB**. *RouterA* and *RouterB* have already established a *GRE over IPsec* tunnel between the two sites.
1. *HostA* prepares a packet for transmission and sends it to the *RouterA*
2. *RouterA* uses **GRE** to encapsulate the original packet with a *GRE header* and a new *IP header*
3. *RouterA* uses [[CCNA/20 - Definitions/IPsec\|IPsec]] to encapsulate and encrypt the *GRE packet* with an *IPsec VPN header* and new *IP header*
4. *RouterA* sends the *GRE*-encapsulated packet *over* the *IPsec*-encrypted tunnel to *RouterB*
	1. See what I did there? GRE over IPsec?
5. *RouterB* decrypts the *IPsec* packet, then *decapsulates* the *GRE* packet
6. *RouterB* delivers the *original* data packet to *HostB*


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources

