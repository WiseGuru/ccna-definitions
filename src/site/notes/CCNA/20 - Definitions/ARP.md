---
{"dg-publish":true,"permalink":"/ccna/20-definitions/arp/","tags":["defs_ccna"]}
---

Exists at [[CCNA/20 - Definitions/21 - OSI Layers/Layer 2\|Layer 2]], ARP maps IP addresses to [[CCNA/20 - Definitions/MAC Address\|MAC]] addresses
- ARP requests and replies are [[CCNA/20 - Definitions/802.3 Frames\|Frames]] that include the target [[CCNA/20 - Definitions/IPv4 Address\|IP address]], the sender's [[CCNA/20 - Definitions/MAC Address\|MAC Address]], and either the [[CCNA/20 - Definitions/Broadcast Address\|Broadcast]] or target's [[CCNA/20 - Definitions/MAC Address\|MAC]] Address
	- If the [[CCNA/20 - Definitions/Switch\|Switch]] doesn't have the know the target [[CCNA/20 - Definitions/MAC Address\|MAC]] address, it broadcasts out the request to all ports
	- Hosts that receive frames with mismatched target [[CCNA/20 - Definitions/MAC Address\|MAC]] addresses will drop the frame
	- The source and destination IP addresses never change
	- The [[CCNA/20 - Definitions/MAC Address\|MAC]] address changes at each hop
	- At each hop, the ARP cache is updated to expedite future requests.
- Mapped addresses are saved to a host's ARP Cache and the Switch's [[CCNA/20 - Definitions/MAC Address\|MAC]] Address Table, which allows the host to send unicast [[CCNA/20 - Definitions/Unicast Address\|Unicast]] packets directly to the destination
- When sending an ARP request outside of the [[CCNA/20 - Definitions/IP subnet\|subnet]], the host will first contact its [[CCNA/20 - Definitions/Default Gateway\|Default Gateway]]
	- Sender wants to send ARP request to destination outside of its [[CCNA/20 - Definitions/IP subnet\|subnet]]
	- It first sends an ARP request to its Default Gateway's [[CCNA/20 - Definitions/IPv4 Address\|IP address]]
		- the DG replies with its own [[CCNA/20 - Definitions/MAC Address\|MAC]] address
	- The sender then sends a request with the Target's IP, but uses the DG's [[CCNA/20 - Definitions/MAC Address\|MAC]] address
	- The DG then forwards the ARP request to the appropriate [[CCNA/20 - Definitions/IP subnet\|subnet]]
		- The target replies with its [[CCNA/20 - Definitions/MAC Address\|MAC]] address
	- The DG then forwards to reply to the sender




# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources



> [!info]- Created (dynamic):: 
> Date created (stamp): 2023-11-05
> Updated:: 


