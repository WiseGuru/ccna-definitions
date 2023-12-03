---
{"dg-publish":true,"permalink":"/ccna/20-definitions/ios-storage-locations/","tags":["defs_ccna"],"created":"2023-11-05T10:55:11.000-08:00","updated":"2023-11-08T13:59:52.945-08:00"}
---

- **ROM**
	- *Read-Only Memory*
	- Like a BIOS; first loaded on device power-up
		- Performs Power On Self Test (POST)
		- Load's Bootstrap
			- Bootstrap looks for an IOS image in Flash
	- If no IOS image found, will load ROMMON
		- ROM MONitor can be used to recover missing or corrupted images
- **Flash**
	- Built-in on older devices; newer devices use CompactFlash
	- Used to store IOS images
		- IOS images can be loaded with TFTP or USB
	- First IOS image in storage gets loaded
		- Can override with `Config# boot system flash (image name)`
- **NVRAM**
	- *Non-Volatile RAM*
		- Does not wipe on power loss
	- Stores the startup-config file
	- After the system has loaded the IOS image, it will check for a startup config
		- If found, startup-config is copied to RAM as running-config
		- If not found, initiates Setup Wizard
- **RAM**
	- *Random Access Memory*
		- Wipes on power loss
	- Runs the running-config
		- Any changes to running-config must be copied to startup-config to persist between power outages


1. Configuration storage locations
	1. The IOS OS image is stored in flash
	2. The startup config is stored in NVRAM
	3. The running config is loaded into RAM on bootup

1. The VLAN Database ([[CCNA/20 - Definitions/Switch\|switches]] only)
	1. On a [[CCNA/20 - Definitions/Switch\|Switch]], the VLAN database (vlan.dat) is saved in either Flash or NVRAM, depending on the model of [[CCNA/20 - Definitions/Switch\|Switch]]

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources

