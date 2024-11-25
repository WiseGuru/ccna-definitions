---
{"dg-publish":true,"permalink":"/20-definitions/southbound-api/","tags":["defs_ccna"]}
---

#### Southbound Interface/[[20 - Definitions/API\|API]]
- *Southbound APIs* or *Southbound Interfaces (SBIs)* connect the Control Layer and the Data Layer in the [[20 - Definitions/SDN\|SDN]]
- There are a few common *SBIs* 
	- **NETCONF**
	- **OnePK**
	- **OpFlex**
	- **OpenFlow**


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/netconf/#netconf" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### NETCONF
1. *Network CONFiguration protocol (NETCONF)* is a [[20 - Definitions/Southbound API\|Southbound API]] that  ([[20 - Definitions/IETF\|IETF]], 2006) was designed as a replacement for [[20 - Definitions/SNMP\|SNMP]]
	1. Uses [[20 - Definitions/XML\|XML]] and [[20 - Definitions/RPC\|RPCs (Remote Procedure Calls)]] to configure network devices
	2. Typically uses [[20 - Definitions/SSH\|SSH]] (sometimes [[20 - Definitions/TLS\|TLS]]) for transport
2. NETCONF and [[20 - Definitions/YANG\|YANG]] provide a standardized way to programmatically inspect and modify the configuration of a network device





</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/one-pk/#one-pk" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### OnePK
- *OnePK* is a #Cisco-Proprietary [[20 - Definitions/Southbound API\|Southbound API]]
- It uses [[20 - Definitions/JSON\|Java]], C, or [[20 - Definitions/Python\|Python]] to configure network devices
- It relies on [[20 - Definitions/SSH\|SSH]] or [[20 - Definitions/TLS\|TLS]] for transport







</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/open-flow/#open-flow" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### OpenFlow
- OpenFlow is a [[20 - Definitions/Southbound API\|Southbound API]] that uses an *imperative* [[20 - Definitions/SDN\|SDN]] model that sends detailed instructions to the data plane when new policy is configured (unlike [[20 - Definitions/OpFlex\|OpFlex]])
- The SDN Controller manages *both* the *network* and the *policies* applied to the devices







</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/op-flex/#op-flex" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### OpFlex
- OpFlex  is a [[20 - Definitions/Southbound API\|Southbound API]] that uses a *declarative* [[20 - Definitions/SDN\|SDN]] model, where the instructions are not super detailed (unlike [[20 - Definitions/OpenFlow\|OpenFlow]])
	- Allows the devices on the data plane to make more network decisions about how to implement policy







</div></div>








# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
