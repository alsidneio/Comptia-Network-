Devices: 
	- routers and switches, they are derived from hubs and bridges
	- **HUB** is a **LAYER-1** device that connects multiple devices and workstations #Network-plus-Definitions 
		- Passive hub: just repeats the information 
		- Active Hub: Repeats information and boost signal for , amplification restarts the 100 meter limit
			- Use an active hub for long distances. 
		- hubs create a bigger collision domain 
		- ![[Pasted image 20240308123035.png]]
	- **BRIDGE** is a  **LAYER2**  device that helps decrease domain collision issues of a hub #Network-plus-Definitions 
			- bridges analyz source MAC addresses and makes intelligent forwarding decisions based on the destinsation MAC in the frames
			- ![[Pasted image 20240308124311.png]]
			- ![[Pasted image 20240308123210.png]]
		- **SWITCH** is a **LAYER2** device  and is known as a mutliport bridge #Network-plus-Definitions 
			- a switch connects multiple network segments together
			- breaks up collision domains, confines them to the individual ports, creates a full duplex situations 
				- all ports are part of the same broadcast domain 
				- Broadcast domain is: how many known devices in the route table #Network-plus-Definitions 
			- makes forwarding decisions like a bridge
			- Layer 2 devices focus on MAC addresses 
			- there are layer 3 switches,  that can perform like a router but in a less efficient manner
			- **anytime you hear  a switch mentioned you are talking about layer2 device unless otherwise noted**
			- ![[Pasted image 20240308123158.png]]
			- 
		- **ROUTER** is  a **LAYER3** device  #Network-plus-Definitions 
			- A router connects multiple networks together
			- makes forwarding decisions based on logical network info
			- Routers can seperate broadcast domains 
			- ![[Pasted image 20240308123142.png]]


network device table #notecard 

| Device Type       | Collision Domains | Broadcast Domains | OSI Layer |
| ----------------- | ----------------- | ----------------- | --------- |
| Hub               | 1                 | 1                 | 1         |
| Bridge            | 1 per port        | 1                 | 2         |
| Switch            | 1 per port        | 1                 | 2         |
| Multilayer Switch | 1 per port        | 1 per port        | 3+        |
| Router            | 1 per port        | 1 per port        | 3+        |
## Additional Ethernet Switch features
---
- Link Aggregation  (IEEE 802.3ad) #notecard
	-  congestion can occur when all ports can operate at the same speed 
	- combine all the data and send them out on different ports 
	- allows two or more links to pass network traffic as if they were one physical link?

- Power over Ethernet/ POE+ (PoE 802.3af/ PoE+ 802.3at) #notecard 
	- supplies electrical power over ethernet & requires cat 5 or higher copper cable
	- each cable supplies 15.4/25.5 watts respctively #notecard 
	- PSE: Power SOurcing equipment give power 

- Port Monitoring/ Port Mirroring 
	- Packet monitoring using a network sniffer on a hiub
	- packet monitoring is done via mirroring via switch 
	- port mirroring is copying traffic on one port to another port 

- User Authentication (802.1x) #notecard 
	- Requires users to authenticate before accessing a network
- Switch/Router Management Access & Authentication #notecard 
	- SSH over port 22: remote administration 
	- console port: rst serial cabel , must be on site 
	- Out of band Management network 
		- is a network the connects and configures devices 
- First Hop redundancy #notecard 
	- For switches and routers
	- Uses Hot Standby Router Protocol HRSP to create virtual IP and MAC addr to provide active and standby routers
	- devices connected talk to virtual router then forwards request to active router
	- Other Protocols for load management
		- Gateway Load Balancing Protocol **GLBP**
		- Virtual Router Redundancy Protocol **VRRP**
		- Common Address Redudancy Protocol **CARP**
- Mac filrering
	- denying or allowing traffic based on a device's mac address
- Traffic Filtering 
	- allows or denies traffic based on IP addresses or application ports
- Quality of Service QoS
	- Forwards traffic based on priority markings 
	- you can tell a switch or router which traffic is more important 
