---
{"dg-publish":true,"dg-path":"20 - Definitions/EAP.md","permalink":"/20-definitions/eap/","tags":["defs_ccna"]}
---

#### EAP
- *Extensible Authentication Protocol* is the authentication framework that other wireless authentication methods are built on
	- Integrated into [[CCNA/20 - Definitions/802.1X\|802.1X]]
- EAP Methods
	1. *LEAP (Lightweight EAP)*
		1. Developed by Cisco
		2. Vulnerable, should not be used anymore
		3. Clients provide credentials
		4. Mutual authentication occurs
	2. *EAP-FAST* (EAP Flexible Authentication via Secure Tunneling)
		1. Developed by Cisco
		2. Three phases
			1. a [[CCNA/20 - Definitions/PAC\|PAC]] (Protected Access Credential) is generated and passed from the server to the client
			2. a secure TLS tunnel is established between the client and the authentication server
			3. Inside the encrypted TLS tunnel, the client and server authenticate
	3. *PEAP* (Protected EAP)
		1. Like EAP-FAST, it creates a secure TLS tunnel
			1. Instead of a PAC, the server uses a digital cert for authentication and establishing a TLS tunnel
			2. Client still needs to authenticate with credentials through the tunnel, like with [[CCNA/20 - Definitions/CHAP\|MS-CHAP]] (Microsoft Challenge-Handshake Authentication Protocol)
	4. *EAP-TLS* (EAP [[CCNA/20 - Definitions/TLS\|Transport Layer Security]])
		1. Requires both client and server authenticate using certificates outside of the tunnel
			1. However, TLS tunnel still used to exchange encryption key information
		2. Most secure, but most difficult to implement


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources

