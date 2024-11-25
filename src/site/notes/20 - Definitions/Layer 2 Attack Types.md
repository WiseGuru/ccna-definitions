---
{"dg-publish":true,"permalink":"/20-definitions/layer-2-attack-types/","tags":["defs_ccna"]}
---

#### [[20 - Definitions/VLAN\|VLAN]] Hopping
- *Double-tagging [[20 - Definitions/dot1q\|802.1Q]]* frames on a *trunk* link to move between VLANs
- Mitigate by *disabling DTP*, change the *native VLAN* to an unused VLAN, and configure all user-facing interfaces as *access ports*

#### [[20 - Definitions/MAC Address\|MAC]] Flooding (or [[20 - Definitions/CAM Table\|CAM Table]] Overflow)
- An attacker floods a switch with frames to *overwhelm* a switch's MAC table
	- The switch stops making forwarding decisions, and all traffic is *flooded*
	- The attacker is able to *view all traffic* being sent *on the switch*
- Mitigate by configuring [[20 - Definitions/Port Security\|Port Security]] with a *maximum* number of allowed MACs on *Access* ports

#### MAC Spoofing
- An attacker *spoofs* a *valid MAC* address to impersonate another device and bypass *port security*
- Possibly mitigate *port security* with *sticky MACs*
	- Also possibly [[20 - Definitions/DAI\|DAI]] to validate IP and MAC address associations
- **[[20 - Definitions/AAA\|AAA]]** and **[[20 - Definitions/802.1X\|802.1X]] with device certificates** are the *actual solution*, but are probably **not on the CCNA**

#### [[20 - Definitions/DHCP\|DHCP]] Spoofing
- An Attacker inserts a rogue *DHCP Server* to intercept and *redirect* traffic
- Mitigate with [[20 - Definitions/DHCP Snooping\|DHCP Snooping]] to restrict *DHCP traffic* to *trusted ports*

#### [[20 - Definitions/ARP\|ARP]] Poisoning (or ARP Spoofing)
- An attacker sends *[[20 - Definitions/Gratuitous ARP\|Gratuitous ARP]]* messages to a host, associating the attacker's *MAC* address with another host's valid *IP* address
- Mitigate with [[20 - Definitions/DAI\|DAI]] to intercept and validate *ARP* messages



# Metadata
### OSI or TCP/IP Layer
[[15 - OSI Layers/Layer 2\|Layer 2]]

### CCNA Exam Topic

### Contributors

### Sources
