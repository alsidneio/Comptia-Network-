## Routing Fundamentals
---
- **Router**: Forwards traffic between subnets, between an internal and external nertwork, or between two external networks
- Each subnet  or external network is going to be its own broadcast domain 
- routers are used to seperate broadcast domains L3
- switches separate collision domains
- Multilayer switch for the exam functions as a router

#### How routing works
---
- switches use mac addresses to route traffic
- router uses ip addressing to route traffic 

## Routing tables
---
- A routing table helps determine which route entry is the bes fit for the network
	- Each entry in a table has a prefix, the longer the prefix the more specific that network is 
	- the longest really means how many octets are defined
#### Route connection types
---
- Directly connected router: physically cconnected routers
	- directly connected routers share routing tables
-  Static routes: routes configured manually by an administrator
	- default static route: 0.0.0.0/0
	- the default static route  says: IF YOU DONT KNOW WHERE TO GO, JUST GO HERE
- Dynamic routing: learned by exchanging information between routers via dynamic protocols 
		- dynamic routing chooses the best route via: How many hops, Bandwith available, etc 

- Preventing routing loops: 
	- split horizon: prevents a route learned on one interface from being advertised back out of that same interface 
	- Posion reverse: causes a route recveived on one interface to be adverised back out of that same interface with a metric considered to be infinite
	- 

| Destination Network | Next Router | Port | Route Cost |
| ------------------- | ----------- | ---- | ---------- |
| 125.0.0.0           | 137.3.14.2  | 1    | 12         |
| 161.5.0.0           | 137.3.6.6   | 1    | 4          |
| 134.7.0.0           | 134.17.3.12 | 2    | 10         |

## Routing Protocols
---
#### Router Advertisement Method
---
###### Convergence
- Convergence is the time it takes for routers to update their routing tables in response to a topology change
- Converged Network: When all routers know about all the other routers 
- to speed up convergence time: 
	- Use a Hold-down Timer: Prevents updates for a specific period of time
###### Route Believability
- if a route has a lower administrative distance ,AD, the route is more believable
- RIp is less believable osfp
- the lower the beliveablity the better the score
- directly connected: 0
- statically connected: 1 
- EIGRP:  90
- OSFP: 110
- RIP: 120
- External EIGRP: 170
- Unknown/Unreachable: 255
###### Distance Vector
- sends full copy of routing table to its directly connected neighbors at regular intervals
- Concerns:
	- This has a slow convergence time 
	- Hop count:  Number of routers from the source router through which data must pass to reach the destination network
	- distance vectors do not consider speed in routing 

###### link state
- requires all router to know about the paths that all other routers can reach in the network
	- specifically the cost and connection speed
-  Has a faster convergence time than the distance vector
###### Protocols
Interior Protocols: 
- Routing information Protocol, RIP
	- A distance vector protocol that uses hop count (maximum hops of 15; 16  is infinite)
	- Updates every 30s 
	- easy to configure
	- runs over UDP
- Open Shortest Path First, OSPF
	- link state protocol that uses cost as its factor
	- cost is based on link speed between routers
- Intermediate System to Intermediate System, IS-IS
	- A link state protocol that also uses cost and functions lik OSPF, but not as widely popular
-  Enhanced Interior Gateway Routing Protocol, EIGRP
	- an advanced distance vector protocols that uses bandwith and delay
	- this is only available on Cisco only networks
 
External Protocols: 
- Border Gateway Protocol, BGP
	- A path vector that uses the number of autonomous system hops instead of router hops 
		- How Many systems do I have to go through 
		- this protocol is the backbone of the internet
		- widespread utilization 
		- has VERY slow convergence

## Address Translation NAT & PAT
---
Address translation came about as a stop gap for running out of ipv4 addresses

- Network Address Translation: 
	- used to conserve limited supply of IPV4 addresses
	- it translates your private ip to public ip for routing 
	- there are 4 types of NAT IP addresses: 
		- inside local: Private Ip Address referencig an inside device 
		- inside global: Public IP address referencing an inside device 
		- outside local: private IP referencing an outside device 
		- outside global : public IP referencing an outside device


#### Types of Address Translation 
----
- DNAT: Dynamic NAT
	- Automatically assigns an IP address from a pool and givers a one-to-one translation
	- works well when only a few hosts need access to the internet at a given time
	- Think about it like DHCP for address translation: 
		- a public ip is leased out, then returned when work is complete
- SNAT:  Static NAT
	- manually assigning private and public ips
- PAT: Port address translation 
	- Shares one public IP via multiple private IPs addresses which gives a many to one translation
	- Most common in use today

## Multicast Routing 
---
Multicast sender send traffic to a class D IP address, known as a multicast group

goal: send traffic out once to all devices 

###### PRotocols
- Internet Group Management, IGMP
	- Lets routers know which interfaces hacve multicast recivers and allows clients to join a multicast group
	- Three versions of IGMP
		- v1: every 60s the multicaster confirms that the device still wants to be in casting group
		- v2: added functionality for client to send leave message to exit group, router assumes you wantr t be ther
		- v3: added functionality for client to request multicast from specific server and allowed source specifc mutlicast  and multiple video streams into a single mutlicast stream 

- Protocol Independent Multicast , PIM
	- ROutes multicast traffic between routers and forms a multicast distribution tree
	- this can cause a big hit to bandwith before it prunes the route 
	- PIM SM is the generally used mode because of the upfront costs, and eventual convergence on shortest path