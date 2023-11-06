---
{"dg-publish":true,"permalink":"/ccna/20-definitions/dce/","tags":["defs_ccna"]}
---

#### DCE/DTE
DCE/DTE are two sides of a [[CCNA/20 - Definitions/Serial\|Serial]] connection.
1. The **DCE** (*Data Circuit-terminating Equipment, Data Communications Equipment, or Data Carrier Equipment*) transmits the clock signal and controls the clock rate
2. The **DTE** (Data *Terminal* Equipment) receives the clock signal
3. Summary:
	1. **DCE** Transmits the clock signal and controls the clock rate
	2. **DTE** Receives the clock signal

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


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources



> [!info]- Created (dynamic):: 
> Date created (stamp): 2023-11-06
> Updated:: 


