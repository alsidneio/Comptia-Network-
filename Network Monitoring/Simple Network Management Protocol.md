- An internet protocol for collecting, organizing, and modifying information about managed devices on IP networks #Network-plus-Definitions 

- Managed device: any device that can communicate with an SNMP manger or the Management information Base (MIB) #Network-plus-Definitions 

 - SNMP needs a manager and agents to work. 

- SNMP Manager: Any machine on the network that is running the SNMP protocol to collect and process information from the devices #Network-plus-Definitions 
- SNMP Agents: Network devices that send information about themselves to the SNMP manager #Network-plus-Definitions 
	- Agents use 3 different message types: 
		- set: manager --> agent request 
			- changes value of variables or list of variables 
		- get: manager --> agent request
			- retrieve value of variables or list of variables
		- trap: agent --> Manager
			- async notification from agent to manager 
			- think events or alarm information 

#### SNMP Traps 
---
- Data in snmp are sent and stored in a k-v pair configuration
- 
Encoding SNMP Trap messages 
- Granualar trap: 
	- each snmp trap message is sent with a unique object ID, OID
	- OID identifies a variable 
	- THe OID is translated to the Management Information Base, MIB
		- MIB: the management data structure of deviece subsytem using a heirarchial namespace
		- MIB saves network bandwidth because of data translation, otherwise we would have to send everything

- Verbose trap:
	- SNMP traps may be configured to contain all the information about a given alert or event as a payload

SNMP versioning 
---
V1,v2,v3
- Information is sent via community strings
	- v1,v2 are sent in plain text 
	- v3 addeded: 
		- integrity via hashing
		- authentication via source validation 
		- confidentiality: data encryption via DES/AES
- V3 groups components into different entities and then gives different authorization and privilges to each group 
	- creates segmentation and enhances security
