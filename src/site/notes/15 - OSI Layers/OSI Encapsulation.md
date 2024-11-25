---
{"dg-publish":true,"permalink":"/15-osi-layers/osi-encapsulation/"}
---

#### OSI Encapsulation
- *OSI Encapsulation* is the process of *encapsulating* and *decapsulating* information for transport at the different layers of the [[15 - OSI Layers/OSI Model\|OSI Model]]
- When a client sends information, it gets packed up into different [[20 - Definitions/PDU\|PDU]]s like a Russian doll from [[15 - OSI Layers/Layer 7\|L7]] to [[15 - OSI Layers/Layer 2\|L2]] before getting sent over the wire



| OSI Layers   | TCP/IP Layers | PDU for each layer | Data Encapsulation (1>7) | Data De-encapsulation (7>1) |     |
| :----------- | :------------ | :----------------- | :----------------------- | :-------------------------- | --- |
| Application  | ---           | Data               |                          |                             |     |
| Presentation | Application   | Data               |                          |                             |     |
| Session      | ---           | Data               |                          |                             |     |
| Transport    | Transport     | [[20 - Definitions/Segment\|Segment]]        | Packets>Segments         | Segment>Packets             |     |
| Network      | Internet      | [[20 - Definitions/Packet\|Packet]]         | Frames>Packets           | Packets>Frames              |     |
| Data-Link    | Data-Link     | [[20 - Definitions/802.3 Frames\|802.3 Frames]]   | Bits>Frames              | Frames>Bits                 |     |
| Physical     | Physical      | [[20 - Definitions/bits\|bits]]           | -                        | -                           |     |

![OSI Encapsulation-2.png](/img/user/CCNA/Attachments/OSI%20Encapsulation-2.png)
Source: Original


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
[OSI Reference Model](https://netcert.tripod.com/ccna/internetworking/osi.html)