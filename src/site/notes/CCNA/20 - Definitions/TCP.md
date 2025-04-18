---
{"dg-publish":true,"dg-path":"20 - Definitions/TCP.md","permalink":"/20-definitions/tcp/","tags":["defs_ccna"]}
---

## TCP
### TCP Summary
*Transmission Control Protocol* is a [[CCNA/15 - OSI Layers/Layer 4\|L4]] connection-oriented protocol
1. Connection oriented
	1. Before transmitting data, two hosts establish a connection
2. Reliable communication
	1. Destination host *MUST* send an acknowledge that it received each TCP [[CCNA/20 - Definitions/Segment\|Segment]]
	2. If a segment isn't acknowledged, it is resent
3. Sequencing
	1. Sequence numbers allow hosts orient segments in the correct order
	2. **Forward Acknowledgement** is used to indicate the sequence number of the next segment the host expects to receive
4. Provides [[CCNA/20 - Definitions/Flow Control\|Flow Control]]
	1. Destination can tell source host to change the flow rate of data.
	2. The TCP header *Window Size* indicates how many segments can be sent before an **ACK** is required for them

#### TCP Header
![TCP-header-2.png](/img/user/CCNA/Attachments/TCP-header-2.png)
	Source: [Wikipedia](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#TCP_segment_structure)
1. The *Source* and *Destination* ports are 16 bits long, so there are **65536** available port numbers
2. The *Sequence number* and *Acknowledgement number* are used to provide sequencing and reliable communication
3. There are a series of flags in the *12th octet* that are used (when set to 1, they are active)
	1. Flags used to establish/terminate connections
		1. ACK
		2. SYN
		3. FIN
4. *Window Size* is used for [[CCNA/20 - Definitions/Flow Control\|Flow Control]]

### TCP Connection Creation and Termination
#### TCP Three-Way Handshake (Creation)
1. HostA initiates with a Segment with the SYN flag set
2. HostB replies with a SYN-ACK flags set
3. HostA responds with the ACK bit set

#### TCP four-way handshake (Termination)
1. HostB initiates termination with a FIN flag
2. HostA responds with an ACK
3. HostA then send it's own segment with a FIN flag
4. HostB responds with an ACK

### TCP Sequencing
TCP uses **Forward Acknowledgement** to sequence messages
1. Each host tracks its own sequence of messages with the *Sequence number*
2. Each host indicates the next messages sequence number it expects to receive with the *Acknowledgement number*
3. Example of a 3-way handshake and future dataflow:
	1. HostA *starts* communication with a *SYN* segment and a *random sequence number* of 27
		1. In practice, the random numbers are much larger and do not increment by 1
	2. HostB responds with a *SYN-ACK* segment with a *random sequence number* of 3, and an *acknowledgement number* of 28
		1. The *acknowledgement number* is in anticipation of receiving a segment with that sequence number
	3. HostA Responds with an *ACK* segment with a *sequence number* of 28, and an *acknowledgement number* of 4
	4. HostB responds with segment with a *sequence number* of 4, and an *acknowledgement number* of 29
	5. etc.
### Common Protocols
Port 21, [[FTP\|FTP]]
Port 22, [[CCNA/20 - Definitions/SSH\|SSH]]
Port 23, [[CCNA/20 - Definitions/Telnet\|Telnet]]
Port 53, [[CCNA/20 - Definitions/DNS\|DNS]]
Port 80, [[CCNA/20 - Definitions/HTTP\|HTTP]]
Port 443, [[CCNA/20 - Definitions/HTTP\|HTTPS]]


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-1-5 
### Contributors

### Sources
[Transmission Control Protocol - Wikipedia](https://en.wikipedia.org/wiki/Transmission_Control_Protocol)