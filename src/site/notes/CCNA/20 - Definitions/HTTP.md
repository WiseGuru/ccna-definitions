---
{"dg-publish":true,"permalink":"/ccna/20-definitions/http/","tags":["defs_ccna"]}
---

### HTTP
- Hypertext Transfer Protocol is used to share and request information

#### HTTP Requests

##### HTTP Verbs
1. GET
	1. Retrieves data from the server
	2. Idempotent
	3. Includes sensitive information in the [[CCNA/20 - Definitions/URI\|URI]], which can be logged
2. PUT
	1. Updating an existing resource or create a new resource of it doesn't exist
	2. Idempotent
3. POST
	1. Creating a new resource
	2. Not idempotent (multiple identical requests results in different outcomes)
	3. Does not include form data in the request *URI*; instead, form data is encoded in a [[CCNA/20 - Definitions/URL\|URL]], and calls a function on the server to process the information
4. HEAD
	1. Retrieving metadata about a source without fetching the actual data
		   	1. HTML standard prevents HEAD requests from containing message body/form data
		   	2. Typically only used to extract header information or test HTML links
	2. Idempotent


Format and examples:

![HTTP-1.png](/img/user/Attachments/HTTP-1.png)

![OSI Encapsulation-1.png|600](/img/user/Attachments/OSI%20Encapsulation-1.png)

#### HTTP Response Codes
1. **1xx** - Informational
	1. The request was received, continuing process 
2. **2xx** - Successful
	1. The request was successfully received, understood, and accepted
3. **3xx** - Redirection
	1. Further action needs to be taken in order to complete the request
4. **4xx** - Client Error
	1. The rest contains bad syntax or could not be fulfilled
5. **5xx** - Server Error
	1. The server failed to fulfill an apparently valid request
![HTTP-ResponseCodes-1.png](/img/user/Attachments/HTTP-ResponseCodes-1.png)




# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources



> [!info]- Created (dynamic):: 
> Date created (stamp): 2023-11-06
> Updated:: 


