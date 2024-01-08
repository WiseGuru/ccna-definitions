---
{"dg-publish":true,"permalink":"/ccna/20-definitions/ssh/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-07T13:54:59.000-08:00"}
---

#### SSH
- *Secure Shell* is a cryptographic network protocol for secure data communication, remote shell services, or command execution, and other secure network services between two networked computers
	- Communicates over [[CCNA/20 - Definitions/TCP\|TCP]] port 22
- There are several prerequisites to configure *SSH* on a Cisco device
	- Cisco IOS image must be a **k9(crypto)** image to support encryption
	- Specify a *hostname*
	- Define a *domain name*
	- Generate [[CCNA/20 - Definitions/RSA\|RSA]] key pairs with a *modulus* of at least *768* bits for *SSHv2*

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
[Configure SSH on Routers and Switches - Cisco](https://www.cisco.com/c/en/us/support/docs/security-vpn/secure-shell-ssh/4145-ssh.html)