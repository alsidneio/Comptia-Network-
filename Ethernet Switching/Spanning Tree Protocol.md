## Spanning Tree Protocol STP 802.1d
---
**Function**: Permits redundant links between switches and prevents looping of network traffic #Network-plus-Definitions 

this is important due to service of reliability: 5-9s , 5 mins of downtime per year. 

- Scenario: there are multiple ways to get to a destination device,  so copies of packets continue to get forwarded indefinitely 
	- Broadcast Storm: Mutiple copies of frames being forwarded back and forth which then consumes the network, this can be avoided with STP 
	- STP use root & non root bridge: 
		- root: switch with the lowest bridge ID **BID**, that switch is allowed to act as a reference point for that entire Spanning tree #Network-plus-Definitions 
			- BID is made up of a Priority ID and MAC Address
				- if all priorities are equal then you choose the lowest MAC address
		- non-root: Every other switch in the network typology #Network-plus-Definitions 
			- root port:  the port on all non-root bridge that is closest in terms of cost
				- cost is determined by speed. Slower cables have higher cost , faster cables have a lower cost. 
				- if speed is equal it will be the lowest port number. 
			- designated port: the port of a network segment that is closest to the root bridge in terms of cost #Network-plus-Definitions 
				- all ports on the root bridge are considered designated ports
			- non-designated port, NDP: Ports that block traffic to create a loop free topology for STP function
				- NDPs receive bridge protocal Data Units BPDUs #Network-plus-Definitions 
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
