network monitoring comes in two forms: 
- Full Packet capture
	- can take up a lot of memory very quickly
	- FPC captures the entire packet, header and payload
- Netflow Data, Flow analysis
	- Records metadata and statistics about netwrok traffic using a flow collector
	- wont have the full packet data , beut detaild metadata on network traffic
	- visualization that gives network map 

#### Netflow tools
---
- Netflow: Cisco developed means of reporting netflow infomatation to a structured DB #Network-plus-Definitions 
	- AKA IPFIX
	- Defines traffic flow bases on different packets that share the same characteristics
	- information you can glean in this tool: 
		- Network protocol interface 
		- IP version/type
		- source/destination IP address
		- IP service type

- Zeek 
	- a hybrid tool that passively monitors networks like a sniffer
	- however it will do full packet capture on the "interesting" packets 
		- intersting packets are based on configuration
	- Does data normalization and stores it in tdf, or JSON text file

- Multi Router Traffic Grapher MRTG: 
	- used to create graphs to show network traffic flows going through network interfaces on different routers and switches
