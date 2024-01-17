---
{"dg-publish":true,"permalink":"/ccna/20-definitions/ttl/","tags":["defs_ccna"]}
---

#### TTL
- *Time-to-live* or *hop limit* is a mechanism which limits the lifespan or lifetime of data in a computer or network. Once the number of hops exceeds the TTL, the packet is dropped. 

## Not relevant for the CCNA
Typically, *TTL*s begin at *255*, *128*, and *64*. If you are reviewing a [[CCNA/20 - Definitions/PCAP\|PCAP]] file in [[CCNA/20 - Definitions/Wireshark\|Wireshark]], and you're seeing [[CCNA/20 - Definitions/TCP\|TCP]] **RESET** packets with a TTL of 64, it means that packet was not routed, and was most likely blocked by a [[CCNA/20 - Definitions/Firewall\|Firewall]]. 

# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
[Time to live - Wikipedia](https://en.wikipedia.org/wiki/Time_to_live)
[Technical Tip: Analyzing TCP RST (Reset) packets i... - Fortinet Community](https://community.fortinet.com/t5/FortiGate/Technical-Tip-Analyzing-TCP-RST-Reset-packets-in-Wireshark/ta-p/269330)