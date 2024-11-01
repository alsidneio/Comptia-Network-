- provides authentication and encryption of data packets to create a secure and ecrypted communication path between two computers

### Protection types 
- condifentiality via data encryption 
- integrity - ensuring data is not modified in transit 
- authentication :  verifies parties are who they claim to be 
- anti-replay: checking sequence number on all packets prior to transmission,

### How IPSec Works
---

Key exchange request : request to start exchange 
- request to start a VPN is established 
IKE phase 1: authenticate parties and establish secure connection 
- identities authenticated and encrypted 
- then a public key exchange is negotiaited and validated 
- two ways to do this: 
	- main mode: conducts 3 two way echanges from initiator to receiver sa fofllows
		- agree upon which algorithms and hashes will be used to secure the IKE communication 
		- use Diffie-hellman exchange to generate shared secret to prove identites
		- verify idnentity of ther side by looking at encrypted form of IP address 
	- aggressive mode: faster but less secure than main mode 
IKE phase 2: negotiate security params a fully establish secure tunnel
- negotiate IPSec Security Assocition SA params protected by the existing IKE SA, this allows the following 
	- Establish IPSec SA within the current tunnel, via quick mode 
		- quick mode allows you to renegotiate before time runs out 
	- periodically renegotiate IPSec SAs to maintain security 
	- perform Diffie-Hellman Exchanges if needed
Data transfer: transfer data in the secure tunnel
- two modes for data transfer: 
	- transport mode: 
		- uses packets original IP header to be used for client to site VPNs
		- use case: keeping packet size under a specific MTU
	- Tunneling Mode: 
		- encapsulate the entire packet and use a new header
		- the encapsulation increases the packet size
		- site to sitye VPNS

tunnel termination: timeout or mutual termination or deletion 

#### Key Exchange 
---
Diffie helman key exchange allows toew systems that dont know each other to be able to exchange keyus and trust each other

- IKE phase 1 creates a tunnel to authenticate eachother 
- then a public key is for each machine is made 
- both systems create a shared secret using the diffe-hellman  algo. 
- with the shared secret they create another secured tunnel, THIS IS THEW PHASE 2 KEY and this is where data is exchangedd\

#### Authentication Header
---
Provides connectionless data integrity and data origin authentication for IP datagrams and provides protection against replay attacks
- AH does not contain encryption of the data itself

#### Encapsulating Security Payload ESP
---
provides authrntication integrity replay protection and data confidentiality  

- encrypting the payload and not the headers 
- 