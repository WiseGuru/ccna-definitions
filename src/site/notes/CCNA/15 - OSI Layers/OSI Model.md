---
{"dg-publish":true,"dg-path":"15 - OSI Layers/OSI Model.md","permalink":"/15-osi-layers/osi-model/"}
---



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/15-osi-layers/layer-1/#layer-1-physical" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Layer 1 - Physical
*The Physical Layer (Layer 1)* defines the specifications needed for activating, maintaining, and deactivating the physical link between end devices
- Conveys the bit stream through the network at the electrical, mechanical, and optical level
- Often uses [[CCNA/20 - Definitions/Copper\|Copper]] or [[CCNA/20 - Definitions/Fiber\|Fiber]] 
- Sends binary data in a [[CCNA/20 - Definitions/bits\|bitstream]]



</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/15-osi-layers/layer-2/#layer-2-data-link" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Layer 2 - Data Link
*The Data Link Layer (Layer 2)* defines how data is formatted for transmission and how access to physical media is controlled
- [[CCNA/20 - Definitions/802.3 Frames\|Frames]] are encoded and decoded into bits at [[CCNA/15 - OSI Layers/Layer 2\|Layer 2]].
- Provides error detection for [[CCNA/15 - OSI Layers/Layer 1\|Layer 1]]


</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/15-osi-layers/layer-3/#layer-3-network" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Layer 3 - Network
*The Network Layer (Layer 3)* is responsible for *routing packets* to their destination and for [[CCNA/20 - Definitions/QoS\|QoS]]. It also provides connectivity and path selection between two host systems that may be located on geographically separated networks.




</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/15-osi-layers/layer-4/#layer-4-transport" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Layer 4 - Transport
*The Transport Layer (Layer 4)* provides transparent transfer (i.e. transport) of data between hosts and is responsible for end-to-end recovery and flow control. It defines services to segment, transfer, and reassemble the data for individual communications between the end devices.



</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/15-osi-layers/layer-5/#layer-5-session" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Layer 5 - Session
*The Session Layer (Layer 5)* establishes, manages, and terminates sessions between two communicating hosts



</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/15-osi-layers/layer-6/#layer-6-presentation" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Layer 6 - Presentation
*The Presentation Layer (Layer 6)* ensures that the information that is sent at the application layer of one system is readable by the application layer of another system.




</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/15-osi-layers/layer-7/#layer-7-application" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Layer 7 - Application
*The Application Layer (Layer 7)* provides network services to the applications of the user




</div></div>

