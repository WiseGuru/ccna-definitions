---
{"dg-publish":true,"dg-path":"20 - Definitions/REST.md","permalink":"/20-definitions/rest/","tags":["defs_ccna"]}
---

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
		- Although REST APIs use HTTP, which uses [[CCNA/20 - Definitions/TCP\|TCP]] as its [[CCNA/15 - OSI Layers/Layer 4\|L4]] protocol, HTTP and REST APIs themselves aren't stateful
			- The functions of each layer are separate
	- Cacheable or non-cacheable
		- **Must support caching of data**
			- However, not all resources must be cacheable
		- Cacheable resources must bee marked as cacheable
	- Layered system
	- Code-on-demand (optional)




- Rest APIs are used in [[CCNA/20 - Definitions/SDN\|SDN]] [[CCNA/20 - Definitions/Northbound API\|Northbound APIs]] between the *Control Layer* and the *Application Layer*, allowing devices in those layers to communicate







# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources
