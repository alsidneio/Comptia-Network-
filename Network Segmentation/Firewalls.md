Boundary walls that analyze network traffic as it enters or leaves a network segment #Network-plus-Definitions 
- firewalls use a ser o rules defining the types of traffic permitted or denied through the device #Network-plus-Definitions 
	- SW/HW based 
	- virtual/physical 
	- host based/network based
- A phyisical Firewall device can be used a network address translator NAT, or port address translator PAT

#### Types of Firewalls
---
- Packet filtering Firewall
	- permits or denies traffic based on packet header #Network-plus-Definitions 

- Stateful firewall
	- aka session based firewall
		- prone to phishing tests
	- Inspects traffic as part of a session and recognizes where the traffic originated #Network-plus-Definitions 
	- respects the flow of traffic based on which device in the network made the request

- Netgen Firewall
	- conducts deep packet inspection and packet filtering 
	- they operate at layer  5,6,7

Access COntrol list: A set of rules applied to router interfaces that permit or deny certain traffic #Network-plus-Definitions 

Unified threat management system device, UTM 
	- combines firewall, router,intrusion detection/prevention system, anti-malwarem and other features into a single device #Network-plus-Definitions 

## Configuring Firewalls
---
- specific rules first, generic rules later 
- best practice to include a deny all rule 

Firewall rules have 4 attributes 
	- type 
	- source 
	- destination 
	- action 

Hardware based firewall
