---
{"dg-publish":true,"permalink":"/ccna/20-definitions/25-mnemonics-and-summaries/configuring-routes/"}
---


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/static-route/#configure-a-static-route" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Configure a static route
- [[CCNA/20 - Definitions/IPv4\|IPv4]]
	- `config# ip route <destination address> <netmask> <next-hop add. or local interface> <ad>`
		- Destination address
			- Network address of the target network
		- Netmask
			- [[CCNA/20 - Definitions/IP subnet\|subnet]] mask of the target destination written in dotted-decimal
		- Next-hop Address or Local interface
			- Either the IP address of the directly-connected neighbor interface, or the local interface you want to send traffic out of
		- [[CCNA/20 - Definitions/AD\|AD]] (*Administrative Distance*)
			- Default is **1**, but can be manually set
			- To configure a **Floating Static Route**, assign an *AD* of 1 or more than the 
- [[CCNA/20 - Definitions/IPv6\|IPv6]]
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
		- [[CCNA/20 - Definitions/AD\|AD]] (*Administrative Distance*)
			- Default is **1**, but can be manually set
			- To configure a **Floating Static Route**, assign an *AD* of 1 or more than the 




</div></div>


#### OSPF
- Clear or Reset the OSPF process on the local router
	- `# clear ip ospf process`


#### RIP
- Configure the router to stop sending RIP advertisements out of a RIP-enabled interface
	- `config-router# passive-interface <Interface ID>`




# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
