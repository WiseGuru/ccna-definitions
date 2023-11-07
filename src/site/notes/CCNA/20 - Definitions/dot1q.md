---
{"dg-publish":true,"permalink":"/ccna/20-definitions/dot1q/","tags":["defs_ccna"]}
---

#### dot1Q
- [[CCNA/20 - Definitions/IEEE\|IEEE]] **802.1Q** encapsulation tags [[CCNA/20 - Definitions/21 - OSI Layers/Layer 2\|Layer 2]] [[CCNA/20 - Definitions/802.3 Frames\|frames]] for trunking
- Dot1Q trunks are configured on the links between [[CCNA/20 - Definitions/Switch\|switches]] where we need to carry traffic for multiple VLANS
	1.  ISL (Inter-Switch Link) was a Cicso Proprietary trunking protocol, now obsolete
	2.  When the [[CCNA/20 - Definitions/Switch\|Switch]] forwards traffic to another [[CCNA/20 - Definitions/Switch\|Switch]], it tags the layer 2 Dot1Q header with the correct VLAN
	3.  The receiving [[CCNA/20 - Definitions/Switch\|Switch]] will only forward the traffic out ports that are in that VLAN
	4.  The [[CCNA/20 - Definitions/Switch\|Switch]] removes the Dot1Q tag from the Ethernet frame when it sends it to the end host
1. *PCP* (Priority Code Point) field can be used to identify high/low priority traffic

### 802.1Q tag
- **4 bytes**
- First **two bytes** is the *TPID (Tag Protocol ID)*, which is **0x8100**
	- This indicates that the frame is *tagged for VLANs*
- Last **two bytes** is the *TCI (Tag control information)*, and contains the *PCP*, *DEI*, and *VID*
	- *Priority Code Point (PCP)*
		- 3-bit field identifying Class of Service ([[CCNA/20 - Definitions/CoS\|CoS]])
	- *Drop eligible indicator (DEI)*
		- 1-bit field that indicates if a frame can be dropped when the network is congested
	- *VLAN Identifier (VID)*
		- 12-bit field identifying the frame's [[CCNA/20 - Definitions/VLAN\|VLAN]], allowing up to *4,094 VLANs*
			- 12-bits = 4096 total possible values *minus* top and bottom (*0* and *4095*)

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources



> [!info]- Created (dynamic):: 
> Date created (stamp): 2023-11-06
> Updated:: 


