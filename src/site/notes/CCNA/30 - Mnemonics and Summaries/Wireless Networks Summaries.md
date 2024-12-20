---
{"dg-publish":true,"dg-path":"30 - Mnemonics and Summaries/Wireless Networks Summaries.md","permalink":"/30-mnemonics-and-summaries/wireless-networks-summaries/"}
---

#mnemonics

- [[CCNA/20 - Definitions/CSMA-CA\|CSMA/CA]] (Carrier Sense Multi-Access with Collision Avoidance) is used to avoid collisions in wireless networks (like [[CCNA/20 - Definitions/CSMA-CD\|CSMA/CD]] in wired networks)
- [[CCNA/20 - Definitions/WPA Authentication Modes\|WPA Authentication Modes]]
	- *PSK* = **Personal**
	- *[[CCNA/20 - Definitions/802.1X\|802.1X]]* = **Enterprise**
- WLC Trivia
	- When creating Interfaces, you first *Name* the interface, then assign a *VLAN ID*
	- When mapping a *WLAN* to a *VLAN,* you're asked for these properties in order:
		- **Type**
			- Almost always WLAN
		- **Profile Name**
			- Used to identify the WLAN on the WLC
			- Usually the same as the SSID
		- **SSID**
		- **ID**
			- Unique number that identifies the WLAN in the WLC
			- Specific number or order doesn't matter
			- Automatically increments
	- Enable WPA+WPA2 PSK Authentication
	- ![WLAN-WPA2-PSK-Config-1.png](/img/user/CCNA/Attachments/WLAN-WPA2-PSK-Config-1.png)
		- WLAN Tab>Edit WLAN
		- Security Subtab>[[CCNA/15 - OSI Layers/Layer 2\|Layer 2]] Subtab
		- Choose *WPA+WPA2*
		- Check the box for *WPA2 Policy*
- VLAN QoS
	- *Platinum* = Voice
	- *Gold* = Video
	- *Silver* = Best Effort, default
	- *Bronze* = Background

### Wireless Signal Disruption
- **ARRDSI**
	- *Absorption*
		- Signal is absorbed in material and converted to heat
	- *Reflection*
		- Signal bounces off material
	- *Refraction*
		- When the wave is broken up because it's slowed down by the medium it's passing through
		- Refraction, literally "to break up"
	- *Diffraction*
		- When a signal is split around an object, creating a blindspot
		- Diffraction, literally "to break apart"
	- *Scattering*
		- Physical interference, like dust, smog, uneven surfaces, etc.
	- [[CCNA/20 - Definitions/Interference\|Interference]]
		- Signal interference, like other WLAN connections, microwaves, etc.

### Wireless Signal Anatomy
- **FAPH**
	- *[[CCNA/20 - Definitions/Amplitude\|Amplitude]]*
		- The size of each cycle/oscillation in a wave
	- *Period*
		- The time it takes for one cycle/oscillation to take place.
		- The *Period* is the reciprocal of the *Frequency*
			- Period = 1/frequency
	- *Frequency*
		- The number of cycles/oscillations per unit of time.
		- The *Frequency* is the reciprocal of the *Period*
			- Frequency = 1/period
	- *Hertz*
		- Cycles per second
			- The unit of measurement for *Frequency*
		- kHz = 1,000 cycles per second
		- GHz = 1,000,000,000 cycles per second
- In 2.4GHz Wifi, there are *13 (technically 14) channels* available
	- Each channel is *22 MHz* wide
	- Avoid overlapping channels by choosing channels *1, 6, and 11*

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-2-9 #extop-2-6 
### Contributors

### Sources
