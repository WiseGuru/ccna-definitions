---
{"dg-publish":true,"permalink":"/ccna/20-definitions/udp/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-12T18:23:43.000-08:00"}
---

### UDP
*User [[CCNA/20 - Definitions/Segment\|Datagram]] Protocol* is a best-effort [[CCNA/20 - Definitions/21 - OSI Layers/Layer 4\|Layer 4]] protocol
1. UDP segments are called **datagrams**
2. *Not* connection-oriented
	1. No connection is established before data is transmitted by the host
3. *Does Not* provide reliable communication
	1. Acknowledgements are not sent, and lost segments are not retransmitted
	2. Segments are sent *best-effort*
4. *Does Not* provide sequencing
	1. If sequences arrive out of order, there is no mechanism to reconstruct them in order
5. *Does not* have flow control
	1. No mechanism like [[CCNA/20 - Definitions/TCP\|TCP]]'s *Window Size* to control flow of traffic
6. Best used for streaming video/audio content
#### UDP Header
![UDP-header-1.png](/img/user/Attachments/UDP-Header-1.png)
Source: [Wikipedia](https://en.wikipedia.org/wiki/User_Datagram_Protocol#UDP_datagram_structure)
#### Common protocols and ports:
Port 69,  [[CCNA/20 - Definitions/TFTP\|TFTP]]
Port 161, [[CCNA/20 - Definitions/SNMP\|SNMP]]
Port 53, [[CCNA/20 - Definitions/DNS\|DNS]]

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic
#extop-1-5
### Contributors

### Sources
[User Datagram Protocol - Wikipedia](https://en.wikipedia.org/wiki/User_Datagram_Protocol)