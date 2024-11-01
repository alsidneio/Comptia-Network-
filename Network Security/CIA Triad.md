### Confidentiality: Safety and Privacy
---
- encryption and authentication 
- encryption ensures that it cant by read by only the intended person
- Encryption types: 
	- Symmetric Encryption #Network-plus-Definitions 
		- Both sendwe and receiver use the exavt same key to encode/decode the message
		- symmetric encryption is fast but also cumbersome
		- the biggest issue is getting the intended users the key 
			- key mannagement is the headache at scale
	- Asymmetric Encryption #Network-plus-Definitions 
		-  sender and receiver use two different keys
		- solves the issue of key management , but at a cost of speed
		- RSA is the most used implementation 
		- RSA uses Public Key Infrastructure PKI #Network-plus-Definitions 
			- key exchanges are facilitated through encrypted messages: Public and private key pair
			-
### Integrity: Ensuring data was not modified in storage or transit
---
- hashing: algorithm that creates a unique Identifier, Hash, based on some data
- hashes must match for data intiegrity

### Availability: how accessible is data
---
vulnerabilities: 
	- crashing devices byf sending improperly formatted data: PING of death attack 
	- flood a network with too much data to prosses: Denial of Service attack
	- Power outages
	- devices dying old age
	- 