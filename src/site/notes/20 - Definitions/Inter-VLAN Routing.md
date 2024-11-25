---
{"dg-publish":true,"permalink":"/20-definitions/inter-vlan-routing/","tags":["defs_ccna"]}
---

- Router with Separate Interfaces
	- Routers configure each interface to a different [[20 - Definitions/VLAN\|VLAN]]
	- Less likely to suffer congested lines, but more likely to run out of interfaces
- [[20 - Definitions/ROAS\|Router on a Stick]]
	- Traffic for multiple VLANs are trunked on a single interface
	- Each VLAN is assigned to a virtual sub-interface
	- More likely to suffer congested lines
	- The [[20 - Definitions/dot1q\|dot1q]] tag in a [[20 - Definitions/802.3 Frames\|Frame]] specifies the sub-interface
- Layer 3 Switch
	- Takes over some Layer 3 functions of a router, such as local VLAN/Subnet switching
	- Intra-campus traffic routed on switch backplane, reducing hops to external router
	- Router may still be needed for WAN connected and other services
- Configuration
	- Router: Create the sub interface on the [[20 - Definitions/Trunk\|Trunking]] interface
		- `config# int <interface>.<VLAN ID>`
			- That is, `config# int g0/1.10`
	- Router: Configure the sub interface to operate on a specific VLAN
		- `config-subif# encap dot1q <vlan ID>`
		- If the sub-interface belongs to the *native* VLAN, don't forget to add `native` at the end
	- Router: No shut the *main interface* to enable all sub-interfaces
		- `config-if# no shut`
	- Switch: Configure interface to function as a trunk port, with the allowed VLANs
		- `config-if# switchport mode trunk`
		- `config-if# swithcport trunk allowed vlan <VLAN IDs separated by commas>`

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources

