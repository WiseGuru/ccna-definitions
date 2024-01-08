---
{"dg-publish":true,"permalink":"/ccna/20-definitions/wireless-access-points/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-11T11:53:00.977-08:00"}
---

#### Wireless APs
- *Wireless Access Points* provide connectivity between wireless station and between wireless and wired networks
	- Wireless is half-duplex, kind of like a [[CCNA/20 - Definitions/Hub\|Hub]]
		- one device can communicate at a time

##### **APs** operate in 3 different modes
- *Autonomous* (rarely but sometimes called *Local-MAC*)
	- Self-contained system, configured individually
		- RF Parameters, security, QoS, VLANs, etc. are all configured locally
	- Typically connected to a [[CCNA/20 - Definitions/Trunk\|Trunk]] port
- [[CCNA/20 - Definitions/Lightweight APs\|Lightweight APs]] (also called *Split-MAC*)
	- Form a [[CCNA/20 - Definitions/CAPWAP\|CAPWAP (Control and Provisioning of Wireless APs)]] tunnel with the [[CCNA/20 - Definitions/WLC\|WLC]]
		- The *Lightweight AP* handles all real-time operations, like wireless traffic, encryption/decryption, etc.
		- *Media Access Control* duties (RF, security, QoS, authentication, etc.) are all offloaded to the *WLC* via the encrypted tunnel
			- All traffic from the AP is tunneled to the *WLC* through the *CAPWAP*
				- *Control* Tunnel: *5246 UDP*
				- *Data* tunnel: *5247 UDP*
	- *Lightweight APs* connect to *Access Ports*, because all traffic is destined for the *WLC*
- *Cloud-based*
	- Between an Autonomous and Lightweight configuration
	- *Data* is routed *locally*, like an autonomous AP
	- *Management* traffic and *Media Access Control Duties* are tunneled to the *cloud controller*
	- [Cisco Meraki](https://meraki.cisco.com/) is a popular option



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/wireless-service-sets/#service-sets" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Service Sets
1. All devices in a service set share the same SSID (service set identifier)
2. Three main kinds of service sets
	1. **Independent**
		1. *IBSS (Independent Basic Service Set)*, also an "*ad hoc*" network
			1. Two or more devices connect without using an AP
				1. AirDrop, etc.
	2. **Infrastructure**
		1. *BSS (Basic Service Set)*
			1. Clients connect to each other via an AP
			2. a *BSSID* uniquely identifies the AP
				1. The *BSSID is the MAC address* of the AP's radio
				2. It is not the SSID
			3. Wireless devices request to "*associate*" with the BSS
				1. Associated devices are called "clients" or "stations"
			4. The *BSA (Basic Service Area)* is the coverage area around an AP
		2. *ESS (Extended Service Set)*
			1. Two or more BSSs connected over a LAN wired network
				1. BSSs are extensions of the same network
					1. The SSID can be the same
					2. The BSSID will be unique
				2. Each BSS should use a different channel to avoid interference
				3. *Roaming* is when devices travel between BSSs
					1. Assisted Roaming is defined by defined by **IEEE 802.11k**
					2. Fast Transition (FT) Roaming is defined by **IEEE 802.11r**
				4. BSAs should overlap about 10-15%
					1. This reduces interference and ensures a smooth transition
	3. **Mesh**
		1. *MBSS (Mesh Basic Service Set)*
			1. Mesh APs use two radios
				1. One provides BSS to wireless clients
				2. Second provides "backhaul network" used to bridge traffic from AP to AP
			2. At least one AP is connected to the wired network called a *Root Access Point (RAP)*
				1. Other APs are called *MAPs (Mesh Access Points)*
			3. A protocol is used to determine the beast path through the mesh
				1. Similar to dynamic routing protocols
3. The upstream wired network is called the *DS (Distribution System)
	1. Each wireless BSS or ESS is mapped to a VLAN in the wired network
	2. It's possible for an AP to provide multiple WLANs mapped to separate VLANs on the wired network
		1. Each WLAN uses a unique BSSID
		2. The VLANs are trunked to the DS
4. Other devices
	1. an AP in repeater mode rebroadcasts another AP's signal
		1. If there's only one radio, it halves the throughput (send and receive signals have to wait for each other to finish)
		2. With two radios, it can broadcast on one channel, return traffic with the other
	2. A *workgroup bridge (WGB)* acts as a wireless client of another AP, and can be used to connect wired devices to the wireless network
		1. Two kinds
			1. *Universal Workgroup Bridge (uWGB)* is an 802.11 standard that only connects to one device
			2. What Cisco calls *WGB* is #Cisco-Proprietary, and allows multiple wired clients to be bridged to the wireless network
	3. Outdoor Bridge
		1. Can be used to connect networks over long distances without a physical cable







</div></div>



# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-1-1 
### Contributors

### Sources
