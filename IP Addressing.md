- IP Address is a numerical label that is used to identify internet communicating devices on a computer network
- Layer 2 devices control internal netork
- Layer 3 device control routing to external networks

#### Mailing analogy
---
IP address have a format to them like the mailing address 

## IPv4 Addressing 
----
ipv4 uses dotted decimal notation. 
- with 4 slots  using 8 bits each 
- 8 bits can contain values  from 0-255
- subnet mask: used to identify the network and host portions of the network
	- 255.255.255.0 
	- a one in the portion of the subnet mask means that portion of the address is  part of the network portion 
	- a zerio in the subnet mask means that portion is available for hosts.
-  A subnet mask of a 255.255.255.0 can host up to 254 devices
	- devices on addresses 192.168.1.4 &  192.168.1.50 can speak to one another with no router because they are within the same subnet(network)
	- devices on addresses 192.168.1.4 &  192.168.0.100  would need  routers because they are  techinically on different networks 
#### CLASSES OF IPV4 SUBNETS
----
There are 5 classes and they are identified by their 1st octet:
- Class A: 
	- octet: 1-127
	- default subnet: 255.0.0.0
	- Possible host: 16.7 million hosts
- Class B: 
	- octet: 128-191
	- default subnet: 255.255.0.0
	- Possible host: 65,356 hosts
- Class C: 
	- octet: 192-223
	- default subnet: 255.255.255.0
	- Possible host: 256 hosts
- Class D:  This class is reserved for multicasting/ multicast routing
	- A multicast address: A logical identifier for a group of hosts in a computer network 
	- octet: 224-239
	- default subnet:  -
	- Possible host: -
- Class E reserved for research and experimental purposes:  
	- octet: 224-239
	- default subnet: -
	- Possible host: 268 million hosts

#### Subnet masks
---
- If ipv4 address and subnet  mask are in the same class, then the address is called **classful  address**
	- classful subnet mask is the default subnet mask for a class
- subnetting: breaking large networks into smaller parts
	- the process of sectioning a network: **Classless inter-domain routing**  CIDR
		- allows for borrowing some of those host bits and reassigning them to the network portion
		- the slash corresponds to the number of bits 
- public v private IPS
	- public: can be routed to 
		- managed by ICANN
		- can be accessed via the internet
	- private: 
		- generally start with 10, 172, or 192
		- Your private IP gets to the internet via **Network Address Translation NAT**
			- NAT allows for routing of private IPs the public ips
		- How to allocated private address guide: RFC 1918
			-  if 1st octet starts with a 10 
				- IP range: 10.0.0.0 - 10.255.255.255
				- addresses:  16.7 million hosts 
				- class: A
			- if octect starts with a 172.16-172.32
				- ip range: 172.16.0.0-172.31.255.255
				- addresses: 1.05 million
				- class: B
			- if octet starts with 192.168
				- ip range : 192.168.0.0 - 192.168.255.255
				- adresses: 65,536 hosts
				- class: C

#### Special IP Addresses
---
- Loopback address:
	- addr: 127.0.0.0/8
	- Creates a loopback to the host and is oftern used in troubleshooting and testing network protocols on a system 
	-  holds 16 million adresses 
	- Also known as localhost
- AIPIPA addresses: 
	- function: used when a device does not have a static IP or cannot reach a dhcp server
	- addrs start with 169.254/16
	- DHCP process: Discover Offer Request Acknowlege

#### Virtual IP Addresses & Sub interfaces
---
- Virtual  IP address, VIP 
	- an Ip adress that does not cvorrelate to an actual physical network interface
	- these addresses are generally used for NAT translation , fault tolerance, and virtualization
- subinterface: 
	- a virtual interface that is created by dividing up a one physical interface into multiple logical interfaces
	- virtual interfaces can be assigned virtual ips 
	- subinterfaces are commonly used in vlans

## IPV4 DataFlows 
----
1. Unicast: single source single destination
	1. 
2. multicast: single source, to multiple but specific destination
3. broadcast: single source to all hosts on a network destination

## Assigning IP Addresses
---
- static assignment: 
	- MANUALLY ASSSIgn **ip, host and default gateway, dns server**
- DHCP(Automatic): 
DNS: converts the domain names used by website to the IP address of trhe server
WINS: DNS for  a windows environments 

#### Dynamic assignment  protocols
----
BOOTP: Bootstrap Protocol 
	- dynamically assigns IP and allows a workstation to load a copy of their boot image over the network
	- used a static table of IP and mac addresses 
DHCP: Dynamic Host Configuration Protocol
- Assigns an IP based on an assignable scope or pool of addresses and provides the ability to configure numerous other oiptions within it
- Form the pool of IPs the server leases the ip for a period of time
- DHCP is the modern implementation of BOOTP
APIPA: Automatic Private IP Addressing
- used when a device does not have a static ip address or cannot reach a DHCP server
- allows for the quick configuration of a LAN withouth the need for aDHCP server
- downside is that they cannot communincate outside the LAN, the router does not recognize the address
- you absolutely cannot get to the internet
ZeroConf:
- newer APIPA with new features
	- zeroconf: can resolve compter names to IP addresses without the need for DNS by using  multicasti domain name service mDNS 
	- can perform a network discovery service 

## Computer Mathematics 
---
decimal to binary conversion

## Subnetting
---
- subnet masks modify the network and create better scopes 
- for a network like 10.0.0.0/8, it has 16.7 million address
	- Can be broken down into the following with 254 host addresses: 
		- 10.0.0.0/24
		- 10.0.1.0/24
		- 10.0.2.0/24
- furst ip is the network ID, last ip is the broadcast ID
	- this is why the number of assignable IPs have to subtract 2 
- Borrowed bits give you the number of networks 
- host bits give avail, give the ip range 
- the slas notation is cidr notation 
- variable length subnet mask 
	- 