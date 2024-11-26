---
{"dg-publish":true,"dg-path":"20 - Definitions/Data Serialization.md","permalink":"/20-definitions/data-serialization/","tags":["defs_ccna"]}
---

#### Data Serialization
- *Data Serialization* is the process of converting structured data to a standardized format that allows sharing or storage of the data in a form that allows recovery of its original structure
	- Example formats include [[CCNA/20 - Definitions/XML\|XML]], [[CCNA/20 - Definitions/JSON\|JSON]], [[CCNA/20 - Definitions/YAML\|YAML]]

<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/xml/#xml-sample" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



###### XML Sample
```XML
<IPInterfaces>
	<entry>
		<Interface><FastEthernet0/0</Interface>
		<IP-Address>192.168.1.1</IP-Address>
		<Status>up</Status>
		<Protocol>up</Protocol>
	</entry>
</IPInterfaces>
```




</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/json/#json-sample" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



###### JSON Sample
```JSON
"ArrayOfObjects":[
{
"name":"Object1",
"number":420,
"boolean_value":false,
"ArrayofNumbers":[420,69,3],
"Nullvalue":,
},
{
"name":"Object2",
"ipaddress":"192.168.1.1"
}
]
```



</div></div>


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/20-definitions/yaml/#yaml-sample" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">



###### YAML Sample
```YAML
---
NETWORKING:
	domain_name: cisco.com
	domain_name_servers: [171.70.168.183]
	networks:
	- gateway: 192.168.50.1
	  pool: [192.168.50.100 to 192.168.50.2504
	  segments: [management, provision]
	  subnet: 192.168.50.0/24
	  vlan_id: 105
```

</div></div>



# Metadata
### OSI or TCP/IP Layer

### CCNA Exam Topic

### Contributors

### Sources

