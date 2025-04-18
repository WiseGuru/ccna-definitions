---
{"dg-publish":true,"dg-path":"20 - Definitions/LAN Topology.md","permalink":"/20-definitions/lan-topology/","tags":["defs_ccna"]}
---

#### LAN Topology
- The campus [[CCNA/20 - Definitions/LAN\|LAN]] should be designed for scalability, performance, and security

### Three Layers in Traditional Design
1. 3-Tier network
2. Core layer
	1. Connect [[CCNA/20 - Definitions/Router\|routers]] to Distribution layer switches
	2. Typically deployed in redundant pairs with downstream Distribution Layer [[CCNA/20 - Definitions/Switch\|switches]] connected to both
	3. Because software policies slow switches down, they should be delegated to Distribution Layer switches
3. Distribution layer
	1. Aggregation point between Access layer and Core layer
	2. Often deployed in redundant pairs
	3. Most software policies, such as [[CCNA/20 - Definitions/QoS\|QoS]], are enabled at this layer
4. Access Layer
	1. Bottom layer, connected to end hosts
	2. Interfaces configured with low-trust, high-flexibility
	3. Often no redundancy between access switches

### Collapsed Distribution and Core Design 
1. Two-tier network
1. Used in smaller campuses that do not need the scalability of three separate layers
2. As the name suggests, the *Core* and *Distribution* layers are collapsed into a *single layer* that performs the functions of both

### Spine-Leaf Network Design
1. Two-tiered network
	1. Sometimes called a *Clos Network* (for Charles Clos)
	2. Often used with [[CCNA/20 - Definitions/Cisco ACI\|Cisco ACI]]
2. Designed for East-West scalability
	1. All spine switches are connected to all leaf switches, BUT
	2. Spine switches *don't connect* to spine switches
	3. Leaf switches *don't connect* to leaf switches
3. Leaf Switches connect to [[CCNA/20 - Definitions/EPG\|EPG]]s (server groups) and [[CCNA/20 - Definitions/Cisco APIC\|Cisco APIC]]s
	1. APICs are typically deployed in clusters of three controllers
		1. Since they are not directly involved in forwarding traffic, they do not have to connect to every spine or leaf
		2. APICs connect to leaf nodes to reduce strain on spine nodes and free up ports on spine nodes
4. Ensures 2-hop maximum for any server to talk to another one
	1. This means there is consistent latency and reliable communication
**Cisco ACI is basically just Spine-Leaf Architecture**

### SOHO Networks (Small Office/Home Office)
1. Typically provided by a single device, often called a "home router" or "wireless router"
2. This one device can provide:
	1. [[CCNA/20 - Definitions/Router\|Router]]
	2. [[CCNA/20 - Definitions/Switch\|Switch]]
	3. [[CCNA/20 - Definitions/Firewall\|Firewall]]
	4. [[CCNA/20 - Definitions/Wireless Access Points\|Wireless AP]]

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-1-2 
### Contributors

### Sources
