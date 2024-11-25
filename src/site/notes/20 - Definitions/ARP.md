---
{"dg-publish":true,"permalink":"/20-definitions/arp/","tags":["defs_ccna"]}
---

#### ARP
- *Address Resolution Protocol (ARP)* maps [[20 - Definitions/IPv4\|IP address]] to [[20 - Definitions/MAC Address\|MAC]] addresses at [[15 - OSI Layers/Layer 2\|Layer 2]]
- ARP requests and replies are [[20 - Definitions/802.3 Frames\|Frames]] that include the target [[20 - Definitions/IPv4\|IP address]], the sender's [[20 - Definitions/MAC Address\|MAC Address]], and either the [[20 - Definitions/Broadcast Address\|Broadcast]] MAC address or the target's [[20 - Definitions/MAC Address\|MAC]] Address
	- If the [[20 - Definitions/Switch\|Switch]] doesn't have the know the target [[20 - Definitions/MAC Address\|MAC]] address, it broadcasts out the request to all ports
	- Hosts that receive frames with mismatched target [[20 - Definitions/MAC Address\|MAC]] addresses will drop the frame
	- The source and destination IP addresses never change
	- The [[20 - Definitions/MAC Address\|MAC]] address changes at each hop
	- At each hop, the ARP cache is updated to expedite future requests.
- Mapped addresses are saved to a host's **ARP Cache** and the Switch's [[20 - Definitions/MAC Address\|MAC]] Address Table, which allows the host to send unicast [[20 - Definitions/Unicast Address\|Unicast]] packets directly to the destination
- When sending an ARP request outside of the [[20 - Definitions/IP subnet\|subnet]], the host will first contact its [[20 - Definitions/Default Gateway\|Default Gateway]]
	- Sender wants to send ARP request to destination outside of its [[20 - Definitions/IP subnet\|subnet]]
	- It first sends an ARP request to its Default Gateway's [[20 - Definitions/IPv4\|IP address]]
		- the DG replies with its own [[20 - Definitions/MAC Address\|MAC]] address
	- The sender then sends a request with the Target's IP, but uses the DG's [[20 - Definitions/MAC Address\|MAC]] address
	- The DG then forwards the ARP request to the appropriate [[20 - Definitions/IP subnet\|subnet]]
		- The target replies with its [[20 - Definitions/MAC Address\|MAC]] address
	- The DG then forwards to reply to the sender




# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-5-7
### Contributors

### Sources

