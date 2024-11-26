---
{"dg-publish":true,"dg-path":"20 - Definitions/DHCP Snooping.md","permalink":"/20-definitions/dhcp-snooping/","tags":["defs_ccna"]}
---

#### DHCP Snooping
- *DHCP Snooping* inspects [[CCNA/20 - Definitions/DHCP\|DHCP]] packets to prevent networking problems and attacks from rogue DHCP servers
- Compares addresses on the *DHCP Snooping binding* table
	- The *binding* table records the Client's *MAC* address, *IP* address, IP *Lease* time, and *VLAN* to its *interface*
		- ![DHCP Snooping-1.png](/img/user/CCNA/Attachments/DHCP%20Snooping-1.png)^[Source: Original]
	- [[CCNA/20 - Definitions/DAI\|DAI]] also uses the *Snooping table* in its frame validation
- It identifies ports as *Trusted* or *Untrusted*
	- **Trusted** ports *forward all DHCP* messages without inspection
	- **Untrusted** ports *act on all DHCP* messages
		- *Discard* DHCP *server* messages
		- *Inspect* DHCP *client* messages
			- **Forwards** messages that *match* its configured information on the *DHCP snooping table*, and **discards** messages that *don't match*
				- **Discover/Request** DHCP Messages
					- Check the frame's *source MAC* and the DHCP message's *CH***ADDR** (Client Hardware Address, i.e. the client's MAC address) fields match
				- **Release/Decline** DHCP Messages
					- Check the *source IP* and receiving *interface* match the entry on the *binding* table
- *Rate Limiting*
	- Automatically *disables interfaces* that send more requests than a configured threshold
	- [[CCNA/20 - Definitions/Error Disabled\|Error Disabled]] interfaces can be *manually* or *automatically* returned to service
- DHCP *Option 82* (aka `information option`)
	- Optionally and only sent by *DHCP relay agents* on messages they *forward* to the *DHCP Server*
		- Provides information about *which relay agent* is forwarding the message, the *VLAN*, *interface*, etc.
	- By default, DHCP Snooping *tags all messages* from clients with *option 82*
		- However, [[CCNA/15 - OSI Layers/Layer 2\|Layer 2]] Switches **drop** incoming DHCP packets with Option 82 on *untrusted ports* by default
		- Similarly, Cisco Routers acting as DHCP server will drop 
			- Error message keywords:
				- `inconsistent relay information`
				- `relay information option exists, but giaddr is zero`
		- It is therefore important to *disable option 82* when configuring DHCP Snooping
			- `config# no ip dhcp snooping information option`



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/dhcp/#dhcp-operations" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



### DHCP Operations
#### **DORA**: DHCP Operations Order
1. **Discover**: DHCP Discover (**Client**, *Broadcast*)
2. **Offer**: DHCP Offer (**Server**, *Unicast/Broadcast*)
3. **Request**: DHCP Request (**Client**, *Broadcast*)
4. **Ack**: DHCP Ack (**Server**, *Unicast/Broadcast*)
#### DHCP Server messages
1. *OFFER*
	1. Initial response to a client request
2. *ACK*
	1. Provisioning of IP address and DHCP information
3. *NAK*
	1. Decline's a user's request for provisioning
		1. Opposite of an ACK
#### DHCP Client Messages
1. *DISCOVER*
	1. Initial packet searching for a DHCP server
2. *REQUEST*
	1. IP address/DHCP information provisioning request
3. *RELEASE*
	1. Release of leased IP address
4. *DECLINE*
	1. Decline offered IP address by a server


</div></div>




### DHCP Snooping config
1. Enable IP DHCP snooping
	2. `config# ip dhcp snooping`
2. Assign a VLAN to be snooped
	1. `config# ip dhcp snooping vlan <vlan ID>`
3. Disable IP DHCP snooping information
	1. `config# no ip dhcp snooping information option`
4. Trust the server-facing interface
	1. `config-if# ip dhcp snooping trust`
5. Check DHCP snooping table
	1. `#sho ip dhcp snooping binding`
6. Configure DHCP rate limiting
	1. `config-if-range# ip dhcp snooping limit rate <allowed messages per second>`
7. Configure errdisable recovery
	1. `config# errdisable recovery cause dhcp-rate-limit`
	2. `# show errdisable recovery`



# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-5-7 
### Contributors

### Sources
[Configuring DHCP Snooping - Cisco Systems](https://www.cisco.com/en/US/docs/general/Test/dwerblo/broken_guide/snoodhcp.html#wp1074087)


