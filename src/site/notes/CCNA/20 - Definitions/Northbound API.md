---
{"dg-publish":true,"permalink":"/ccna/20-definitions/northbound-api/","tags":["defs_ccna"],"created":"2023-11-04T12:45:23.000-07:00","updated":"2023-11-08T14:27:34.000-08:00"}
---

#### Northbound Interface/[[CCNA/20 - Definitions/API\|API]]
- *Northbound APIs* or *Northbound Interfaces (NBIs)* connect the Control Layer and the Application Layer in the [[CCNA/20 - Definitions/SDN\|SDN]]
- There are a few notable *NBIs* that are worth mentioning
	- **REST**
		- *REST* is the most commonly used *NBI*
	- **OSGi**
		- Less frequently used than REST


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/rest/#rest" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### REST
- *Representational State Transfer* APIs are also known as *REST-based APIs* or *RESTful APIs*
	- REST isn't a specific [[CCNA/20 - Definitions/API\|API]]; it describes a set of rules about how the API should work
- There are 6 constraints of RESTful architecture
	- Uniform Interface
	- Client-Server
		- Client uses API calls (like [[CCNA/20 - Definitions/HTTP#HTTP Requests\|HTTP Requests]]) to access resources on the server
		- Separation between the client and server means they can change independently
			- When the client application changes or the server application changes, the interface between them must not break
	- [[CCNA/20 - Definitions/Stateless\|Stateless]]
		- Each API exchange is a separate event, independent of all past exchanges between client and server
			- The server does not store information from previous requests to determine how it should respond to new requests
			- e.g., the client must authenticate with each request
		- Although REST APIs use HTTP, which uses [[CCNA/20 - Definitions/TCP\|TCP]] as its [[CCNA/20 - Definitions/21 - OSI Layers/Layer 4\|L4]] protocol, HTTP and REST APIs themselves aren't stateful
			- The functions of each layer are separate
	- Cacheable or non-cacheable
		- **Must support caching of data**
			- However, not all resources must be cacheable
		- Cacheable resources must bee marked as cacheable
	- Layered system
	- Code-on-demand (optional)




- Rest APIs are used in [[CCNA/20 - Definitions/SDN\|SDN]] [[CCNA/20 - Definitions/Northbound API\|Northbound APIs]] between the *Control Layer* and the *Application Layer*, allowing devices in those layers to communicate








</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/ccna/20-definitions/os-gi/#osgi" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



#### OSGI
- **Java Open Services Gateway initiative (OSGi)** is a Java-based northbound API framework that is intended to enable the development of modular programs
- OSGi also allows the use of [[CCNA/20 - Definitions/Python\|Python]] as a means of extended controller functions
- For transport, OSGi deployments often rely on [[CCNA/20 - Definitions/HTTP\|HTTP]]







</div></div>





# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
