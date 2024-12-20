---
{"dg-publish":true,"dg-path":"20 - Definitions/Lightweight APs.md","permalink":"/20-definitions/lightweight-a-ps/","tags":["defs_ccna"]}
---

#### Lightweight APs
- *Lightweight APs* (also called *Split-MAC Architecture*) split Media Access Control duties between the [[CCNA/20 - Definitions/Wireless Access Points\|AP]] and the [[CCNA/20 - Definitions/WLC\|WLC]]
- Lightweight APs handle "real-time" operations like handling wireless traffic, encryption/decryption, sending beacons, etc.
	- WLCs perform RF/Security/QoS management, client authentication, association, and roaming management, etc.
- *LWAPs* can operate in **8** different modes
	- 

#### Lightweight AP Modes
1. There are two different kinds of modes for Lightweight APs
	1. Client-serving
		1. Local
			1. The default mode that provides [[BSS\|BSS]]s, allowing clients to associate with the WLAN
		2. FlexConnect
			1. Enables traffic switching if the connection to the WLC goes down
			2. Functionally transitions the AP from *Lightweight* mode to *Autonomous* mode
		3. Bridge Mode (also Mesh Mode)
			1. AP forms a dedicated point-to-point or point-to-multipoint bridge between physical networks
		4. Flex+Bridge
			1. Basically what the name says
	2. Network Management
		1. Monitor
			1. Doesn't broadcast an SSID
			2. Monitors *wireless* signals and channels for IDS events, rogue APs, and physically locate other wireless stations
		3. Rogue Detector
			1. Can still broadcast an SSID serving clients
			2. Dedicated to detecting rogue wired and wireless device
		5. SE-Connect
			1. SE stands for [[Cisco Spectrum Expert\|Spectrum Expert]], and collects data for spectrum analysis
			2. Data is sent from the SE-Connect AP to PCs running [[Cisco Spectrum Expert\|Cisco Spectrum Expert]] or [[MetaGeek Chanalyzer\|MetaGeek Chanalyzer]] for review
		6. Sniffer
			1. Functions purely as a wireless traffic receiver (does not broadcast SSID)
			2. forwards all traffic to a machine running [[CCNA/20 - Definitions/Wireshark\|Wireshark]] or [[OmniPeek\|OmniPeek]]


### CLI Commands

With `show ap config general <AP name>`, you are likely to device **addressing** information (DNS, DHCP, Gateway, etc.), but not *Syslog* or other management information
	- You might get *Syslog* info by running `show ap config global` on the [[CCNA/20 - Definitions/WLC\|WLC]] 
This is an example of possible output generated by ChatGPT
```WirelessAP
(Cisco Controller) >sho ap config general AP01

Cisco AP Identifier.............................. 1
Cisco AP Name..................................... AP01
Country code...................................... US
...
Switch Port Number................................ 1
MAC Address....................................... 00:1a:2b:3c:4d:5e
IP Address........................................ 192.168.1.10
IP Netmask........................................ 255.255.255.0
Gateway IP Addr................................... 192.168.1.1
...
DNS server IP..................................... 192.168.1.2
```


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-2-6
### Contributors

### Sources
