IDS/IPS - recognizing or preventing attack 

SNORT IDS: software based IDS 
- IDS is a passive device, will be attatched to a network device as a sidecar #Network-plus-Definitions 
- monitors traffic accross the network and will log and alert if necessary
- detection systems only alert 

IPS: 
- IPS is active device. will be attactched in line of  other network devices  #Network-plus-Definitions 
- will stop and block any data that it thinks its bad
- will do all the things an IDS 
- is the best device to prevent DoS attacks 
- if an IPS is not well tuned it will have a false positive condition and will drop legitimate traffic

Types of Intrustion detection 
- Signature based  
	- traffic that has a unique byte or string pattern #Network-plus-Definitions 
	- 
- policy based 
	- relies on a specific declaration of a security policy
- anomaly based 
	- statistical
		- watches for traffic patterns and flags things outside of the normal 
	- non-statistical 
		- administrator defined baseline pattern

Host based IDS/IPS
- software based IDS that is installed on the host
- clients, server, phones, tablets 
Network based IDS/IPS
- protects the entire network

they both work together to provide stronger security 