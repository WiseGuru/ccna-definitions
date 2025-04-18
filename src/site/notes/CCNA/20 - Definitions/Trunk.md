---
{"dg-publish":true,"dg-path":"20 - Definitions/Trunk.md","permalink":"/20-definitions/trunk/","tags":["defs_ccna"]}
---

#### Trunk
- A *trunk* interface is a single, physical interface that can route traffic to multiple VLANS
- Functions at [[CCNA/15 - OSI Layers/Layer 2\|Layer 2]]
- There are four *Administrative Modes* that can be configured on a switch interface
	- [[CCNA/20 - Definitions/Access port\|access]]
		- A statically configured *access port* will only serve a single data [[CCNA/20 - Definitions/VLAN\|VLAN]]
			- It can be configured to also serve a voice VLAN
	- *trunk*
		- Statically configured to serve as a *trunk* port, and will never become an access port
		- *DTP* is enabled on the interface **unless** it is disabled with `switchport nonegotiate`
			- DTP frames will not be sent, which can prevent an attack from configuring a trunk and [[CCNA/20 - Definitions/Layer 2 Attack Types\|VLAN Hopping]]
		- If connected to an *access* port, it will not form a link
	- *dynamic auto*
		- Configured with **DTP** to *passively form a trunk* if it is connected to a *dynamic desirable* or *trunk* port
		- However, it will not initiate a transition to a trunk, and will remain an *access* port if connected to a *dynamic auto* or *access* port
	- *dynamic desirable*
		- Configured with **DTP** to *actively forma trunk* if it is connected to a *dynamic desirable*, *dynamic auto*, or *trunk* port
		- If connected to an *access* port, it will remain an *access* port
![Trunk-2.png](/img/user/CCNA/Attachments/Trunk-2.png)
Source: Original



# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-2-2 
### Contributors

### Sources
