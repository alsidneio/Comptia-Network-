## Network Time Protocol
---
Coordinates time between different servers,  developed in the 1980s
time is important because security protocols rely on coordinated times 
	- 

NTP works via 
- stratum 
	- each layer of time stratum hierarchy 
	- stratum 0: reference clocks 
		- atomic clock, GPS, and other very accurate time systems 
		- computers cannot sit in stratum 0
	- stratum 1: any computer thats within a  few micro seconds of a stratum 0 clock 
		- Known as Primary Time Servers
	- Stratum2: computer connected ans synchroniized to stratum1
		- configured to query stratum 1 servers 
	- each stratum gets a bit more out of sync 
	- the limit of stratum is 15
- clients
- servers
#### OTher protocols to synchronise time
---
1. Precision time Prrotocol: (PTP)
	- Used to sync time on a computer networ
	- accuracy below microsecond precision
	- uses primary and secondary clocks 
1. Network Time Security
	- is an an extension of NTP 
	- used to provide cryptographic securiity to the NTP 
	- does some authentication and verification of time source
	- Uses TLS and AEAD to ensure authentication