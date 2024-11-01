DHCP:  Dynamic host Configuration Protocol 
	- assigns device with IP addr, provides a subnet mask, default GW and DNS server to talk to 
	- operatates over ports 67 & 68 using UDP #notecard   

DNS: Domain Name System
	-  converts domain names to IP addresses 
	- operates  on port 53 , using  UDP and TCP 
	- uses UDP for Domain name query 
	- uses TCP for a ZONE TRANsfer
		- Zone transfer: When DNS servers share information about associated domain names and IP addrs

NTP: Network Time Protocol 
	- Synchronizes clocks between systems  communicating over packet switched , variable latency data network
	- its really old 
	- uses port 123  over UDP

## DHCP 
---
- Provides an IP addr to every machine on the network and eliminates configuration errors
	- addresses get assigned from an IP scope 
- DHCP Reservation: You can tell DHCP which IPs should be excluded unless they meet certain conditions #Network-plus-Definitions 
- DHCP Process: #notecard 
	- Discover:  I need an ip
	- Offer: do you want this IP
	- Request: yeah ill take it
	- Acknowledgement: lease is handed out
		- general ip lease is set to 24 hours 
- When DHCP assigns an IP  it also gives the following information: #notecard 
	- IP address
	- subnet mask 
	- default gateway 
	- DNS server IP
- What happens if a device cannot reach a DHCP server: 
	- Then your machine defaults to an Automatic Private IP Address, APIPA #notecard 
- DHCP config scope  options 
	- subnet mask 
	- defautl router 
	- dns server 
	- lease time for IP addresses 
	- DHCP relay
- DHCP Relay
	- Forwards DHCP packets between clients & Servers 
	- Used when the client device and the DHCP server are not locaated on the same subnet
	- DHCP uses UDP, so its connectionless, you need an IP helper addr  to help route the packets over the relay 
- IP helper addr
	- Forwards several differen kinds of UDP across the router and can be used in conjucntion with the DHCP relay