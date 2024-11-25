---
{"dg-publish":true,"permalink":"/20-definitions/ad/","tags":["defs_ccna"]}
---

#### AD
- *Administrative Distance* is a measure of how trusted a routing protocol is compared to other protocols
	- However, *AD* does *NOT* determine which route a packet will take, only *whether* it is added to the *routing table* in the event of *duplicate routes*
- A *lower* AD means that a route is *more* trusted
- A **floating [[20 - Definitions/Static route\|Static route]]** is a *[[20 - Definitions/Static route\|Static route]]* with a *higher AD* than the preferred route
	- It is configured as a *backup* should the preferred route fail


| Route source        | Default AD |
| ------------------- | ---------- |
| Connected interface | 0          |
| [[20 - Definitions/Static route\|Static route]]    | 1          |
| [[20 - Definitions/BGP\|BGP]]             | 20         |
| [[20 - Definitions/EIGRP\|EIGRP]]           | 90         |
| [[20 - Definitions/OSPF\|OSPF]]            | 110        |
| [[20 - Definitions/IS-IS\|IS-IS]]           | 115        |
| [[20 - Definitions/RIP\|RIP]]             | 120        |


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-3-2 
### Contributors

### Sources


