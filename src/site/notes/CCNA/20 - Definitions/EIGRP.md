---
{"dg-publish":true,"permalink":"/ccna/20-definitions/eigrp/","tags":["defs_ccna"],"created":"2023-11-05T10:55:11.000-08:00","updated":"2023-11-08T14:33:45.544-08:00"}
---

#### EIGRP
- Enhanced Interior Gateway Routing Protocol
- #Cisco-Proprietary  routing protocol, called "advanced" [[CCNA/20 - Definitions/Distance Vector Routing Protocols\|Distance Vector]] routing protocol
- Much better than [[CCNA/20 - Definitions/RIP\|RIP]], but still a DV protocol
- EIGRP [[CCNA/20 - Definitions/Router\|routers]] need to have the same Autonomous System (AS) number
	- `Config# router eigrp (AS number)`
		- `Config-router# network (Network address) (Wildcard mask)`
			- [[CCNA/20 - Definitions/Wildcard mask\|Wildcard mask]]

### Calculating routes
- **EIGRP Metric** = Bandwidth of *slowest link* + *delay of all links*
- Terminology
	- *Feasible Route* is any route that has a path to the destination
	- *Feasible Distance* is the router's metric value to the route's destination
	- *Advertised Distance* is the neighbor device's *Feasible Distance*
	- **Successor** is the route with the lowest metric to the destination
	- **Feasible Successor** an *guarantied loop-free* alternate route should the *Successor* go down that has a lower *Advertised Distance* than the *Successor's Feasible Distance*
		- The "Lower [[CCNA/20 - Definitions/AD\|AD]] than Successor's FD" is known as the *Feasibility condition*

**NOTE**: I need a graph here to help illustrate all the EIGRP terms.

#### Unequal-Cost Load-balancing
- This is different from [[CCNA/20 - Definitions/ECMP\|ECMP]]
	- By default, EIGRP uses [[CCNA/20 - Definitions/ECMP\|ECMP]]
- You can tell EIGRP to load balance between the Successor and the Feasible Successor routes (ONLY the S and FS routes will be load balanced)
	- Change this via *Metric variance Multiplier*
		- `config-router# variance 2`
			- Variance 2 = *Feasible Successor* with an *FD* up to **2x** the *Successor* route's *FD* can be used to load balance


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources

