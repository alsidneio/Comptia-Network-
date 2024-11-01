- Denial of service attack occurs when one machine is flooding a device with requests for services #Network-plus-Definitions 
	- Usually done with:
		- TCP SYN flood: start a tcp session but never completes...waiting for the timeout build the queue
			- crashes due to resource exhaustion 
			- sender IPs are spoofed to look like new requests 
		- ICMP flood: when an attacker pings to a subnet boradcast 
			- ip is spoofed to make it seem like a different server 
			- all the other devices that heard the brodcast will start responding 
			- 

Distributed DoS: whne multiple machines send a multiple requests #Network-plus-Definitions 
- thius attack is harder in the cloud because of horizontal scaling
- 