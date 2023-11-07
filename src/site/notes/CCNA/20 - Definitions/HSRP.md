---
{"dg-publish":true,"permalink":"/ccna/20-definitions/hsrp/","tags":["defs_ccna"]}
---

#### HSRP
- **Hot Standby Router Protocol** is an [[CCNA/20 - Definitions/FHRP\|FHRP]] protocol
- HSRP uses a Virtual IP (VIP) and [[CCNA/20 - Definitions/MAC Address\|MAC]] address to allow for automated gateway failover
	- The hosts use the VIP as their default gateway address
	- If the active gateway fails, the standby gateway will take over
- Hello messages are sent ever *3 seconds* by default by routes in the *active*, *standby*, or *speak* states
	- Only routers in the *standby* state listen for routers, and takes over if the span between *hello* messages exceeds the *hold time (def. 10 seconds)*
- *VRRP* (Virtual Router Redundancy Protocol) is identical to HSRP, except it uses `vrrp` instead of `standby` for its configuration


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/fhrp/#fhrp-virtual-mac-addresses" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



### FHRP Virtual MAC Addresses
- Virtual MAC addresses
	- HSRPv1: **0.c07.acXX** or 00:00:0c:07:ac:XX
		- 0C7AC
	- HSRPv2: **0.c9f.fXXX** or 00:00:0c:9f:fX:XX 
		- 0C9FF
	- VRRP: **0.5e00.1XX** or 00:00:5e:00:01:XX
		- V = 5e00
		- 05e001 (Oh 5-ee hundred and 1)
	- GLBP: **7.b400.XXYY** or 00:07:b4:00:XX:YY 
		- G =/= 5, so G = b400
		- 7B400


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/fhrp/#fhrp-multicast-address-multicast-addresses" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">




#### FHRP
- First Hop Redundancy Protocols use a Virtual IP (VIP) and [[CCNA/20 - Definitions/MAC Address\|MAC]] addresses to allow for automated failover
- The network clients use the VIP as their [[CCNA/20 - Definitions/Default Gateway\|Default Gateway]]
	- If a physical gateway fails, another gateway will take over

### FHRP Virtual MAC Addresses
- Virtual MAC addresses
	- HSRPv1: **0.c07.acXX** or 00:00:0c:07:ac:XX
		- 0C7AC
	- HSRPv2: **0.c9f.fXXX** or 00:00:0c:9f:fX:XX 
		- 0C9FF
	- VRRP: **0.5e00.1XX** or 00:00:5e:00:01:XX
		- V = 5e00
		- 05e001 (Oh 5-ee hundred and 1)
	- GLBP: **7.b400.XXYY** or 00:07:b4:00:XX:YY 
		- G =/= 5, so G = b400
		- 7B400

### FHRP [[CCNA/20 - Definitions/Multicast Address\|Multicast Addresses]]
- *224.0.0.2*
	- HSRPv1
- *224.0.0.9*
	- RIP
- *224.0.0.18*
	- VRRP
- *224.0.0.102*
	- GLBP
	- HSRPv2

### FHRP Protocols
1. **[[CCNA/20 - Definitions/HSRP\|Hot Standby Router Protocol (HSRP)]]**
	1. Cisco Proprietary; deployed in active/standby pairs
	2. **This is what's covered in the CCNA**
2. Virtual Router Redundancy Protocol (VRRP)
	1. Open standard; deployed in active/standby pairs
	2. Almost identical to HSRP.
		1. One difference is HSRP uses "standby" and VRRP uses "vrrp"
3. Gateway Load Balancing Protocol (GLBP)
	1. Cisco proprietary; supports active/active load balancing across multiple routers on the same subnet

1. FHRP-activated routers communicate with each other by sending **multicast** Hello messages
2. When FHRP is configured, the **Virtual IP address** should be configured as the default gateway for hosts
3. The active FHRP router responds to ARP requests with a **virtual MAC address**
4. HSRP uses **Active** and **Standby** routers
	1. When HSRP Standby router switches to active, it will send **gratuitous ARP messages**
	2. The HSRP active router is determined by **Highest priority**, then **highest IP address**
		1. The default priority is 100
	3. HSRPv1
		1. HSRPv1 Mutlicast address is **224.0.0.2**
		2. Virtual MAC address format: **0000.0c07.acXX**
			1. **(XX is HSRP group number)**
			2. This can be shortened to *0.c07*.acXX
	4. HSRPv2
		1. HSRPv2 Multicast address is **224.0.0.102**
		2. Virtual MAC address format: **0000.0c9f.fXXX**
			1. **(XXX is the HSRP group number)**
				1. This can be shortened to *0.c9f*.fXXX
	5. HSRP Commands
		1. Assign virtual IP
			1. `Config-if# standby (group number) ip (IP address)`
		2. Configure priority
			1. `Config-if# standby (group number) priority (Priority number)`
		3. Configure Preemption
			1. `Config-if# standby (group number) preempt`
		4. Configure Version 2
			1. `Config-if# standby version 2`
5. VRRP uses **Master** and **Backup** routers
	1. VRRP Multicast address is **224.0.0.18**
	2. VRRP Virtual MAC address format is **0000.5e00.01XX**
		1. **(XX = VRRP group number)**
		2. This can be shortened to *0.5e00*.1XX
6. [[CCNA/20 - Definitions/FHRP\|Gateway Load Balancing Protocol]]
	1. Load balances among multiple routers on the same subnet
		1. A single **Active Virtual Gateway (AVG)** is elected
		2. The AVG assigns up to **four** Active Virtual Forwarders **(AVFs)**
	2. [GLBP - Gateway Load Balancing Protocol - Cisco Systems](https://www.cisco.com/en/US/docs/ios/12_2t/12_2t15/feature/guide/ft_glbp.html)
	3. GLBP Multicast address is the same as HSRPv2, **224.0.0.102**
	4. GLBP virtual MAC address format is **0007.b400.XXYY**
		1. This can be shorted to *7.b400*.XXYY
		2. **(XX = GLBP group number, YY = AVF number)**
		3. AVF = Active Virtual Forwarders


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources



> [!info]- Created (dynamic):: 
> Date created (stamp): 2023-11-06
> Updated:: 




</div></div>

### HSRP operations
1.  Both [[CCNA/20 - Definitions/Router\|routers]] have a normal physical [[CCNA/20 - Definitions/IPv4\|IP address]] and [[CCNA/20 - Definitions/MAC Address\|MAC]] address on their HSRP interface
	1.  Unique addresses area used on both [[CCNA/20 - Definitions/Router\|routers]]
2.  They both also have the HSRP VIP and [[CCNA/20 - Definitions/MAC Address\|MAC]] address configured on the interface
	1.  The same addresses are used on both [[CCNA/20 - Definitions/Router\|routers]]
3.  When they come online, one is elected to HSRP active router, the other is standby
4.  The active router owns the virtual IP and [[CCNA/20 - Definitions/MAC Address\|MAC]] address and responds to ARP requests
5.  All traffic for the VIP goes through the active router
6.  The [[CCNA/20 - Definitions/Router\|routers]] send hello messages to each other over their HSRP interface
	1.  If the standby router stops receiving hellos from the active, it will transition to be the active router
	2.  It will take ownership of the VIP and [[CCNA/20 - Definitions/MAC Address\|MAC]] address and respond to ARP requests

### HSRP Router States
1. There are 6 HSRP states
	1. Init
		1. When the link first *comes up*
	2. Learn
		1. The HSRP device is attempting to *learn* the *VIP*
	3. Listen
		1. The device has *learned* the *VIP*
		2. The device is *listening* for *hello* messages from other (*active/standby*) HSRP devices
		3. If a device is not elected to either *active* or *standby*, it remains in the **Listen** state
	4. Speak
		1. The device *sends hello messages* and participates in the *Active router election*
	5. Standby
		1. The device is *actively listening* to *hello* messages from the *Active router*
		2. The default *hold time* is *10 seconds*, roughly 3x the *hello time*
	6. Active
		1. The device *receives data* for and *manages* the *VIP*
		2. Sends *hello messages* ever *3 seconds* (by default)



### Advanced Topics
1. Priority and Preemption
	1. Router priority can be set, with the **higher value** being preferred
		1. Default value is 100
	2. Preemption allows a router to take `Active` when it comes online
		1. Default, preemption is disabled because it can be more stable if there is a fault with the primary router
2. HSRP Version
	1. Version 2 introduced minor improvements
		1. Default version is 1
	2. Both routers must be on the same version
3. Standby Groups
	1. Multiple HSRP "Standby groups" can be configured on interface, allowing for "load balancing" between VLANs or different clients
		1. e.g., R1 is priority in standby 1 10.10.10.1/24, and R2 is priority in standby 2 10.10.20.1/24

### HSRP Configuration
1.  Configure both router interfaces with their IP and "standby IP" (Virtual IP)
	1. Example: VIP is 10.10.10.1
```
R1Config# int g0/1
	Config-if# ip address 10.10.10.2 255.255.255.0
	Config-if# no shut
	Config-if# standby 1 ip 10.10.10.1
	Config-if# standby 1 priority 110
    Config-if# standby 1 preempt
    Config-if# standby version 2
R2Config# int g0/1
	Config-if# ip address 10.10.10.3 255.255.255.0
	Config-if# no shut
	Config-if# standby 1 ip 10.10.10.1
	Config-if# standby 1 priority 90
	Config-if# standby version 2
```
2.  Verification
	1.  `#sho standby`


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources



> [!info]- Created (dynamic):: 
> Date created (stamp): 2023-11-06
> Updated:: 


