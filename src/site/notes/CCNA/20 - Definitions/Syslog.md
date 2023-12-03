---
{"dg-publish":true,"permalink":"/ccna/20-definitions/syslog/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-07T16:01:31.016-08:00"}
---

#### Syslog
- *Syslog* is a standard [[CCNA/20 - Definitions/Logging\|Logging]] format. 
- Each entry follows this format: `seq no:timestamp: %facility-severity-MNEMONIC:description`
	- *seq no*: Sequence number
		- ONLY stamped if `config# service sequence-numbers` is enabled
	- *timestamp*: Date and time of event
		- `config# service timestamps log <datetime/uptime>`
	- *facility*: Service or Hardware generating the message
	- *severity*: 0-7, EACEWNID
	- *MNEMONIC*: Short description (Title)
	- *description*: Detailed information on event

![Syslog-SeverityLevels.png](/img/user/Attachments/Syslog-SeverityLevels.png)





# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
