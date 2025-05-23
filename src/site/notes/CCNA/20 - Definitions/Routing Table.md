---
{"dg-publish":true,"dg-path":"20 - Definitions/Routing Table.md","permalink":"/20-definitions/routing-table/","tags":["defs_ccna"]}
---

#### Routing Table
- The *Routing Table* identifies [[CCNA/20 - Definitions/IP\|IP]] routes to networks
	- The **most specific route** (e.g., the route with the *longest prefix*) is the route that is chosen for any given traffic
- Routes can be [[CCNA/20 - Definitions/Static route\|Static route]] by the administrator, or *dynamically added* through routing protocols like [[CCNA/20 - Definitions/RIP\|RIP]], [[CCNA/20 - Definitions/EIGRP\|EIGRP]], or [[CCNA/20 - Definitions/OSPF\|OSPF]]
- How Routes are selected, from creation to packet forwarding
	- Dynamic Routing Protocols choose routes to advertise based on *Metric*
		- The *Metric* process is different for each protocol
			- **OSPF** uses *cost*, and calculates *reference bandwidth/interface bandwidth*
			- **RIP** does a simple hop count, from *0-15*
			- **EIGRP** boils down to *slowest link* + *delay of all links combined*
	- The router collects all routes that are advertised to it and decides which ones will appear on the table based on *Administrative Distance*
		- [[CCNA/20 - Definitions/AD\|Administrative Distance]] is basically how much the router trusts the route, from *0-255*, with lower being more trustworthy
			- All *Unique routes* from different sources are added to the table
			- If there are multiple *identical routes*, then the one with the *lowest [[CCNA/20 - Definitions/AD\|AD]]* is added
				- Example: Two Three routes are solicited from different protocols
					- Routes:
						- An EIGRP route (*AD 90*) to 172.31.0.0/*16*, on *Fa02*
						- An OSPF route (*AD 110*) to 172.31.0.0/*16*, on *Fa03*
						- An OSPF route (*AD 110*) to 172.30.16.0/*20*, on *Fa01*
						- An EIGRP route (*AD 90*) to 172.30.0.0/*16*, on *Fa04*
					- The *EIGRP* route on *Fa02* will be selected for the table instead of the *OSPF* route on *FA03*
					- The *OSPF* route on *Fa01* AND the *EIGRP* route on *Fa04* will be added to the table, because they are unique
				- **Floating Static Routes** are *identical routes* that are manually configured with a *slightly higher AD* than what's been added to the table, so if the existing route fails, the *floating static route* will fail-over
		- *[[CCNA/20 - Definitions/AD\|AD]] does not impact route selection*, just whether it is added to the table
	- The router receives a packet and sends the packet on the route with the *most specific (longest prefix)* matching network
		- Example: A router receives a packet for 172.31.20.232, and there are four routes to pick from
			- Routes:
				- A static route (*AD 1*) to 172.16.0.0/*8*, on *Fa01*
				- An EIGRP route (*AD 90*) to 172.31.0.0/*16*, on *Fa02*
				- An OSPF route (*AD 110*) to 172.31.16.0/*20*, on *Fa03*
				- An Internal BGP route (*AD 170*) to 172.31.20.0/*24*, on *Fa04*
			- The router will send the packet out of interface *Fa04* because that route has the longest prefix.
	- If there is no matching network on the table, the packet be forwarded out of the *Gateway of last resort*
		- This the catch-all network, `0.0.0.0 0.0.0.0`, and the router that sits between the LAN and the WAN


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/static-route/#i-pv6-routes" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### IPv6 Routes
- There are three kinds of [[CCNA/20 - Definitions/IPv6\|IPv6]] routes
	- *Directly Attached*
		- Only points to the *exit interface*
	- *Recursive*
		- Only points to the *next-hop address*
		- Called recursive because it has to check the routing table twice
			- first to match the destination IP against a route
			- second to match the next-hop address against a route
	- *Fully Specified*
		- Identifies both the *exit interface* and the *next-hop* address


</div></div>


#### Configure a [[CCNA/20 - Definitions/Static route\|Static route]]
`config# ip route <destination> <subnet mask> <next hop> <opt: AD>`
`config# ipv6 route <destination network and mask> <opt: exit interface> <opt: next hop address> <opt: AD>  `


### Routing Metrics and AD
| Protocol               | Type            | AD  | Metric                                           |
| ---------------------- | --------------- | --- | ------------------------------------------------ |
| Connected Interface    | -               | 0   | -                                                |
| Static Route           | -               | 1   | -                                                |
| External BGP           | Path Vector     | 20  |                                                  |
| Internal EIGRP         | Distance Vector | 90  | Bandwidth of *slowest link* and total *Delay*        |
| IGRP (Deprecated)      |                 | 100 |                                                  |
| OSPF                   | Link State      | 110 | *(Ref. Band/Interf. Ban)* |
| IS-IS                  | Link State      | 115 | Cost of all links / config                       |
| RIP                    | Distance Vector | 120 | *Hop count* (All speeds equal)                     |
| External EIGRP         | Distance Vector | 170 | Bandwidth and Delay                              |
| Internal BGP           | Path Vector     | 200 |                                                  |
| Unknown/unusable route |                 | 255 | Route not installed                              |

## Practice Tables






# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-3-1 #extop-3-2 #extop-3-3 
### Contributors

### Sources
