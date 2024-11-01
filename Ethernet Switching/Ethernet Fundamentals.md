## Ethernet fundamentals 
---

10base2, 10base5  were the first ethernet types 

- CAT3: 10BaseT standard and allows 10Mbps 

- Determinisitic v COntention networks 
	- deterministic very organized and orderly communication
		- token rings or token bus works this way
	- COntention :  all devices talking at one time 
		- think about the flow of a conversation 
		- listening for gaps in a conversation 
		-  talking at the same time creates collisions 

Ethernet networks work on the contention based model because of low overhead

- How to detect collisions: 
	- Carrier Sense Multiple Access with Collision Detection (CSMA/CD) #Network-plus-Definitions 
		- prevents collisions by using  carrier sensing to defer transmission until no other stations are transmitting 
		- to help resolve collisions a random backoff number is chosen #Network-plus-Definitions 
	- Collision domain : element of a network that shares a single segment #Network-plus-Definitions 
	- half duplex communication: listening and talking at the same time  #Network-plus-Definitions 
- Keeping network collisions small
	- alot of collisions will cause a lot of retransmission  congestion
	- Ports on Ethernet **switches** or **bridges** create its own collision domain
	- you can operate in full duplex mode when on a switch, which increases speed. 

#### Copper/ethernet vables 
bandwith: how many bits can transmit per second

NOTE: Create cards for the ethernete standards detailed in the Media & [Cabling DOc](obsidian://open?vault=ITOCC&file=Network%2B%2FMedia%20%26%20Cabling%20Distribution)

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

## Spanning Tree Protocal STP 802.1d
---
**Function**: Permits redundant links between switches and prevents looping of network traffic

this is important due to service of reliability: 5-9s , 5 mins of downtime per year. 

- Scenario: there are multiple ways to get to a destination device,  so copies of packets continue to get forwarded indefinitely 
	- Broadcast Storm: Mutiple copies of frames being forwarded back and forth which then consumes the network, this can be avoided with STP 
	- STP use root & non root bridge: 
		- root: switch with the lowest bridge ID **BID**, that switch is allowed to act as a reference point for that entire Spanning tree
			- BID is made up of a Priority ID and MAC Address
				- if all priorities are equal then you choose the lowest MAC address
		- non-root: Every other switch in the network typology
			- root port:  the port on all non-root bridge that is closest in terms of cost
				- cost is determined by speed. Slower cables have higher cost , faster cables have a lower cost. 
				- if speed is equal it will be the lowest port number. 
			- designated port: the port of a network segment that is closest to the root bridge in terms of cost
				- all ports on the root bridge are considered designated ports
			- non-designated port, NDP: Ports that block traffic to create a loop free topology for STP function
				- NDPs receive bridge protocal Data Units BPDUs
				- Transitioning from NDP to DP takes four states: 
					- Blocking: BDPUs are received but not forwarded
					- Listening:  Builds a MAC address table, but does not forward frames
					- Learning: Processes BDPU and determines its roll in the spanning tree
					- Forwarding: becomes a designated port
			- Theres failure detection on non-designated ports to determine if their state needs to be changed. 

Link Cost table 

| Speed    | Ethernet Type    | STP Port Cost |
| -------- | ---------------- | ------------- |
| 10mbps   | Ethernet         | 100           |
| 100 Mbps | Fast Ethernet    | 19            |
| 1Gbps    | gigabit Ethernet | 4             |
| 10Gbps   | 10 gig ethernet  | 2             |

## Virtual Local Area Network, VLAN
---
- VLANs allow the use of a single port to create seperate broadcast domains, different logical networks
	- vlans act as a virtual router


## Specialized Network Devices 
---
#### Virtual Private Network, VPN:
-  Creates a secure VPN/ Virtual Tunnel over an untrusted network 
#### VPN Concentrator
	- terminates VPN tunnels and allow for multiple connections in one location 
	- VPN Headend
		- specific type of concentrator used to terminate the IPSec VPN tunnels with a router or other device
#### Firewall
	- a network security appliance placed at the boundary of a network
		- can be software or HW
		- allow traffic to come in and our of your network
	- Next Generation Firewall
		- conducts deep pack inspection at layer 7 and can look through traffic to detect and prevent attacks
#### Intrusion Detection/ Prevention System 
	- Recognizes and responds to attacks through signatures and anomalies 
	- detection systems can only log the issue 
	- prevention/protection systems will log , and do something about it 
#### Proxy Server
	- a specialized device that makes requests to an external network on behalf of a client 
	- acts as a middle man between host and network
		- function 1: security for content filtering and logging 
		- function 2: serves as seperate cache device for the client
			- this saves bandwith and time by not having to reach out to the internet again.

#### COntent Engine/Caching engine
- Dedicated appliance that performs the caching functions of a proxy server
- the benefit is where data is expensive of slow 
	- think branch offices of a big  office syncing up data
- best for speeding up access to offices

#### Content Switch/Loadbalancer
- distributes incoming request across various servers in a server farm
- Prevents overloading of a single device


## Other Devices
---
VoIP Phone 
- a  HW device that uses your IP network to make a connection to a call manager within your network
- voip phones allow encrypted communications

Unified Communications (Call) Manager
 - used to perform the call processing for hw and software based IP phones

Printers
Security Cameras 
- put them on a seperate vlan , and add ACLs 


