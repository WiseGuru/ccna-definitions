---
{"dg-publish":true,"permalink":"/ccna/20-definitions/roas/","tags":["defs_ccna"]}
---

#### ROAS
- A *Router on a Stick* [[CCNA/20 - Definitions/Inter-VLAN Routing\|Inter-VLAN Routing]] solution creates *sub-interfaces* within a single interface on a router to [[CCNA/20 - Definitions/Trunk\|Trunk]] traffic from different [[CCNA/20 - Definitions/VLAN\|VLAN]]s over a single link between a [[CCNA/20 - Definitions/Switch\|Switch]] and a [[CCNA/20 - Definitions/Router\|Router]]
	- Each VLAN is configured to a unique *sub-interface*
		- The *sub-interface* number *does not* have to match the *VLAN ID*
			- e.g., VLAN 20 can be on interface G0/0.10
		- The [[CCNA/20 - Definitions/dot1q\|802.1Q]] tag in an [[CCNA/20 - Definitions/802.3 Frames\|frame]] identifies the sub-interface
	- The *native VLAN* can be configured on the *main-interface*
- Configuration
	- Router: Create the sub interface on the [[CCNA/20 - Definitions/Trunk\|trunking]] interface
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
