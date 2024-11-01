MTU: largest size of a frame that can be sent
	- max load capacity for a frame within your network
	- TOO high will result in packet loss
	- MTU too small results in increased network overhead

MTU configuration
- standard MTU size for wired ethernet is 1500 bytes #notecard 
- smaller MTU size is used in:
	- wireless networks
	- VPN: Virtual Private network : 1400-1420 bytes
	- PPPoE: Point to point over ethernet 
- Jumbo fram: any frame larger than 1500 bytes 
	- generally configured to be 9000 bytes
	- jumbo frames are good for high available environments
	- fragmentation can occure within a jumbo frame 
	- troubleshooting jumbo frames is a nightmare
	- 