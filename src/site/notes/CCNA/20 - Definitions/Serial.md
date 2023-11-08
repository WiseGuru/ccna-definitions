---
{"dg-publish":true,"permalink":"/ccna/20-definitions/serial/","tags":["defs_ccna"]}
---

#### Serial
- *Serial Interfaces and Cables* transmit data one bit at a time, often in a continuous stream (not parallel, like [[CCNA/20 - Definitions/Ethernet\|Ethernet]])


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/dce/#dce-dte" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### DCE/DTE
- *DCE/DTE* are two sides of a [[CCNA/20 - Definitions/Serial\|Serial]] connection.
	- The **DCE** (*Data Circuit-terminating Equipment, Data Communications Equipment, or Data Carrier Equipment*) transmits the clock signal and controls the clock rate
	- The **DTE** (*Data* **Terminal** *Equipment*) receives the clock signal
- In short:
	- **DCE** Transmits the clock signal and controls the clock rate
	- **DTE** Receives the clock signal

Clock rate only needs to be configured on the DCE
`# sho controllers `
```
R1(config-router)# do sho controllers s0/0/0
Interface Serial0/0/0
Hardware is PowerQUICC MPC860
DCE V.35, clock rate 128000
idb at 0x81081AC4, driver data structure at 0x81084AC0
SCC Registers:
General [GSMR]=0x2:0x00000000, Protocol-specific [PSMR]=0x8
Events [SCCE]=0x0000, Mask [SCCM]=0x0000, Status [SCCS]=0x00
Transmit on Demand [TODR]=0x0, Data Sync [DSR]=0x7E7E
```
The **DCE V.35** indicates that R1 is the DCE in the pair, and controls the clockrate



</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/hdlc/#hdlc" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### HDLC
- *High-Level Data Link Control (HDLC)* is a [[CCNA/20 - Definitions/21 - OSI Layers/Layer 2\|Layer 2]] [[CCNA/20 - Definitions/WAN\|WAN]] Encapsulation Protocol that is used on Synchronous data links
	- [[CCNA/20 - Definitions/Serial\|Serial]] connections use HDLC encapsulation by default
- It has a standard and a #Cisco-Proprietary  version
- **Cisco HDLC** is the default WAN protocol on Cisco devices for [[CCNA/20 - Definitions/Network Types\|point-to-point]] WAN links



</div></div>



# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
