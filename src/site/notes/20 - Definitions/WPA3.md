---
{"dg-publish":true,"permalink":"/20-definitions/wpa-3/","tags":["defs_ccna"]}
---

#### WPA3
- Wi-Fi Protected Access 3 replaced [[20 - Definitions/WPA2\|WPA2]]
- [[20 - Definitions/GCMP\|GCMP]] provides Encryption/[[20 - Definitions/MIC\|MIC]]
	- It uses an equivalent 192-bit cryptographic strength in WPA3-Enterprise mode and mandates the [[20 - Definitions/CCMP\|CCMP]]-128 as the minimum encryption algorithm in WPA3-Personal mode
##### Additional Security Features

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/pmf/#pmf" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### PMF
- *Protected Management Frames (PMF)* is a #Cisco-Proprietary implementation of [[20 - Definitions/IEEE\|IEEE]] 802.11w (Management Frame Protection, MFP)
	- Protects [[20 - Definitions/802.11 Frames\|802.11 management frames]] from eavesdropping and forging by attackers







</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/sae/#sae" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### SAE
- *Simultaneous Authentication of Equals* is a four-way handshake in [[20 - Definitions/WPA Authentication Modes\|Personal Mode]] Authentication that is used by [[20 - Definitions/WPA3\|WPA3]] as an upgrade to the traditional [[20 - Definitions/PSK\|PSK]]






</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/forward-secrecy/#forward-secrecy" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### Forward Secrecy
- Prevents Data from being decrypted after it was transmitted over the air
- Session keys are generated from a long-term [[20 - Definitions/PSK\|Pre-Shared Key]] that is discarded after the session ends
	- Even if the attack obtains the session key, it cannot be used to decrypt past or future sessions





</div></div>




<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/wpa-authentication-modes/#wpa-authentication-modes" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### WPA Authentication Modes
1. All WPA methods support two authentication modes
	1. Personal mode
		1. A [[20 - Definitions/PSK\|Pre-Shared Key]] is used for authentication
			1. The PSK is not sent OTA
			2. A four-way handshake is used for authentication, and the PSK is used to generate keys
		2. Common in small networks
	2. Enterprise mode
		1. [[20 - Definitions/802.1X\|802.1X]] is used with an authentication server (RADIUS/TACACS+ etc.)
		2. All EAP methods are supported








</div></div>





# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
