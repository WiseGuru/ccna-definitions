---
{"dg-publish":true,"dg-path":"20 - Definitions/DNS.md","permalink":"/20-definitions/dns/","tags":["defs_ccna"]}
---

#### DNS
The **Domain Name System** is a hierarchical and distributed naming system for computers, services, and other resources in the Internet or other [[CCNA/20 - Definitions/IP\|IP]] networks. It associates various information with domain names assigned to each of the associated entities. It resolves an [[CCNA/20 - Definitions/FQDN\|FQDN]] to an [[CCNA/20 - Definitions/IPv4\|IP address]] 

Resolved on [[CCNA/15 - OSI Layers/Layer 3\|Layer 3]]
Port 53 [[CCNA/20 - Definitions/TCP\|TCP]]/[[CCNA/20 - Definitions/UDP\|UDP]]


#### Record types
1. *A (Address Record)*
	1. Maps a domain to an IPv4 address
2. *AAAA (IPv6 Address Record)*
	1. Maps a domain to an IPv6 address
3. *CNAME (canonical name)*
	1. Configures an alias for a domain (e.g., \www.example.com CNAME example.com)
4. *MX (Mail Exchange)*
	1. Defines the mail server responsible for receiving mail for that domain
5. *TXT*
	1. Holds text information, like SPF records
	2. Often used for verification
6. *NS (Name Server)*
	1. Specifies the authoritative DNS servers for the domain
7. *PTR (Pointer record)*
	1. Used for reverse DNS lookups
8. *SOA (Start of Authority)*
	1. Provides information about the domain
9. *SRV (service record)*
	1. Specifies location of servers for specific services, like SIP or IMAP
10. *CAA (Certification Authority Authorization)*
	1. Specifies which CAs are allowed to issue certificates for the domain


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extops-4-3
### Contributors

### Sources
[Domain Name System - Wikipedia](https://en.wikipedia.org/wiki/Domain_Name_System)
[What are DNS records? | Cloudflare](https://www.cloudflare.com/learning/dns/dns-records/)
[DNS Records Explained | Gcore](https://gcore.com/learning/dns-records-explained/)
