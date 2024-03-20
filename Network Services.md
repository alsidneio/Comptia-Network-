DHCP:  Dynamic host Protocol 
	- assigns device with IP addr, provides a subnet mask, default GW and DNS server to talk to 
	- operatates over ports 67 & 68 using UDP 

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
- 