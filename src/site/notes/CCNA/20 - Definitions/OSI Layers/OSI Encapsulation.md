---
{"dg-publish":true,"permalink":"/ccna/20-definitions/osi-layers/osi-encapsulation/"}
---

Definition: When sender composes a packet, it gets packed up like a Russian doll from [[CCNA/20 - Definitions/OSI Layers/Layer 7\|L7]] to [[CCNA/20 - Definitions/OSI Layers/Layer 2\|L2]] before getting sent over the wire

[OSI Reference Model](https://netcert.tripod.com/ccna/internetworking/osi.html)

| OSI Layers   | TCP/IP Layers | PDU for each layer  | Data Encapsulation (1>7) | Data De-encapsulation (7>1) | 
|:------------ |:------------- |:------------------- |:------------------------ |:--------------------------- |
| Application  | ---           | Data                |                          |                             |
| Presentation | Application   | Data                |                          |                             |
| Session      | ---           | Data                |                          |                             |
| Transport    | Transport     | [[CCNA/20 - Definitions/Segment\|Segment]]         | Packets>Segments         | Segment>Packets             |
| Network      | Internet      | [[CCNA/20 - Definitions/Packet\|Packet]]          | Frames>Packets           | Packets>Frames              |
| Data-Link    | Data-Link     | [[CCNA/20 - Definitions/802.3 Frames\|802.3 Frames]] | Bits>Frames              | Frames>Bits                 |
| Physical     | Physical      | [[CCNA/20 - Definitions/bits\|bits]]            | -                        | -                           |

![OSI Encapsulation-1.png|600](/img/user/Attachments/OSI%20Encapsulation-1.png)


# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources



> [!info]- Created (dynamic):: 
> Date created (stamp): 2023-11-05
> Updated:: 


