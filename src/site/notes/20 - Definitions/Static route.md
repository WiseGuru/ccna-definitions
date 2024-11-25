---
{"dg-publish":true,"permalink":"/20-definitions/static-route/","tags":["defs_ccna"]}
---

#### Static Routes
- *Static routes* are manually configuring [[20 - Definitions/IP\|IP]] routes entered into a [[15 - OSI Layers/Layer 3\|Layer 3]] device's [[20 - Definitions/Routing Table\|Routing Table]].
- A *Floating Static Route* is a manually-configured *backup route* to another *identical route* with an [[20 - Definitions/AD\|AD]] or *one or more* than the preferred route
	- e.g., a *floating static route* of an [[20 - Definitions/EIGRP\|EIGRP]] dynamic route might have an *AD* set between*91* and *99*
	- A **FSR** won't appear in the routing table (unless the preferred route fails), but will be shown in the *running config*

#### IPv6 Routes
- There are three kinds of [[20 - Definitions/IPv6\|IPv6]] routes
	- *Directly Attached*
		- Only points to the *exit interface*
	- *Recursive*
		- Only points to the *next-hop address*
		- Called recursive because it has to check the routing table twice
			- first to match the destination IP against a route
			- second to match the next-hop address against a route
	- *Fully Specified*
		- Identifies both the *exit interface* and the *next-hop* address

#### Configure a static route
- [[20 - Definitions/IPv4\|IPv4]]
	- `config# ip route <destination address> <netmask> <next-hop add. or local interface> <ad>`
		- Destination address
			- Network address of the target network
		- Netmask
			- [[20 - Definitions/IP subnet\|subnet]] mask of the target destination written in dotted-decimal
		- Next-hop Address or Local interface
			- Either the IP address of the directly-connected neighbor interface, or the local interface you want to send traffic out of
		- [[20 - Definitions/AD\|AD]] (*Administrative Distance*)
			- Default is **1**, but can be manually set
			- To configure a **Floating Static Route**, assign an *AD* of 1 or more than the 
- [[20 - Definitions/IPv6\|IPv6]]
	- `config# ip route <destination address and netmask> <next-hop add. and/or local interface> <ad>`
		- Destination address and netmask
			- The target network address with it's slash-notation subnet mask
				- e.g., 2001:db8::1/64
		- Next-hop address and/or Local interface
			- There are three possible configurations:
				- Directly Connected
					- Only the *local interface* is listed
				- Recursive
					- Only the *neighbor IP address* is listed
					- Called "Recursive" because it has to check the routing table twice
						- It has to check the routing table twice; first to see where to send the packet, next to see which interface is connected to the neighbor IP
				- Fully Specified
					- Identifies *both* the *local interface* and the *neighbor IP*
		- [[20 - Definitions/AD\|AD]] (*Administrative Distance*)
			- Default is **1**, but can be manually set
			- To configure a **Floating Static Route**, assign an *AD* of 1 or more than the 



# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-3-3 
### Contributors

### Sources

