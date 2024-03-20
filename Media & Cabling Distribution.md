## Copper Medium
---

coaxial cable: 
- cable types : 
	- rg-6: cable to the home
	- rg-59: cable  inside the home
- connectors types:
	-   F-type: screw on connector 
	- BNC: lock in place type connector

Twinaxial: 
	- two centers
	- used for short length fast connection
	- 10gbps

Serial cables: 
	- terminated with db9 or db25 connector 

Twisted pair cable:
	- four pairs of twisted cable 
	- more twisting more EFI protection
	- the highter the category, the more twist, more twst more speed
	- UTP: unshielded, media of choice for local area networks
	- STP: shielded , 
		- limitation is about 300 feet
	- COnnectors: 
		- rj45: etrhernet: cat 5,6,7,8, networks
			- only required to use 4/8 pins, the other 4 are used for futrue use 
		- rj11: 6 pin connecter, 2 pins are used , used for phones 
		- pin 1: ring, pin 2: signal 
		- RJ == Registered jack 

Bandwith: Physical lumit of how much data could be transfered
throughput : the actual throughput 

#### Categories of Cabling 
---
- CAT3 (Ethernbet)
	- 10BASE-T
	- 10Mbps
	- 100 meters
- CAT5 (Fast Ethernet)
	- 100BASE-TX
	- 100Mbps
	- 100 meters
- CAT5e (Gigabit Ethernet)
	- 1000Base-T
	- 1000 Mbps (1 Gbps)
	- 100 meters
- CAT6 
	- 1000Base-T or 10GBASE-T
	- 1000 Mbps or 10Gbps
	- 100 meters or 55 meters
- CAT6a
	- 10G BASE-T
	- 1 Gbps
	- 100 Meters
- CAT7
	- 10GBase-T
	- 10 Gbps
	- 100 metes
	- could use bot RJ45 & a TERA connector
- CAT8
	- 40 BASE-T
	- 40 gbps
	- 30 meters

straight through: patch cable 
- use 568B ethernet setup 
- used to connect DTE to DTC 
	- DTE: Data Terminal Equipment: endpoint for concected DCEs
		-  Examples : Laptops , desktop, servers, routers
	- DCE: Data communication Equipment: waypoints for connrected DTEs
		- Example: switches, hubs, modems and bridges

Crossover cable: 
	- used to connect DTE to DTE & DCE to DCE
	- crossocer cables swap the send and receive pins on the connectors 
	- 568A --> 568B
	- pins 1,2,3 and 6  are switched

plemnum v non-plenum
	- fire retardant. has to put in any place that a person cannot see


## Building a Cable 
---
- Straight Thru cable Order,  L --> R:
	- orange/white
	- orange
	- green/white
	- blue
	- blue/white 
	- green
	- brown/white
	- brown
- Crossover cable order . L --> R:  swap pins 1,3 & 2,6
	-  green/white
	- green
	- orange/white
	- blue
	- blue/white 
	- orange
	- brown/white
	- brown

## Fiber Media
---
Fiber optic cable: uses LEDs or laser to transmit information
- Fiber is immune to EMI
- can run a long distance without signal attenuation
- can transmit in the terabit per second range 
- its expensive

#### Fiber cables types
---
Single Mode Fiber, SMF
- used for longer distanses and has a smaller core size which allows for only a single mode of travel for for light signal
- 8.3 -10 microns in diameter
- yellow sheath

Multimode fiber, MMF
- distance == 2 kms or less 
- core is way bigger in multimode
- less expensive than single mode fiber 
- blue/ orange sheet

#### Fiber Connector Types
---
Subscriber Connector, SC:
- sqaure connector that clicks when you push it in 
- each connector only has one mode of transmission. Either a send or receive
Strait Tip, ST:
- Hose looking connector, that twist on to ensure proper connection
Lucent Connector, LC :
- has transmit and receive cable together
Mechanical Transfer Registered Jack, MTRJ:
- smallest connector
- both send and receive are inside the plastic housing 
- usually used in fiber switches, patches 

#### Fiber Interface Types
----
Angled Physical Contact Connector
- fiber end face is angled at 8 degrees
- no signal loss
- green interface
Ultra Physical Contact Connector
- no angle 
- more signal loss
- blue interface 
---

Wavelength Division Multiplexing , WDM 
- combines mutliple signals into one signa and sends them  over a single fiber cable
- uses different wavelengths to differentiate the signals




## Transceivers
--- 
Comparing FIber to copper in the following areas :

1. Bandwidth
2. Distance
3. EMI immunity
4. Security

fiber wins in all of these areas, but coppper is cheaper
Converting  between fiber and copper via transcievers , layer 1 to layer 1 connections

Bidirectional: taking turns communicating on the network, like a walkie talkie
- this is referred to as half duplex communication 
Full duplex communication: 
- allows both device to communicate at the same time 

#### Transceiver Types
---
GBIC
- takes copper connection to routers and allows you to transmit signals via ethernet(RJ45)
Small form-factor pluggable, SFP:
- speed: up to 4.2 Gbps
- called the mini GBIC
SFP+: 
- faster SFP
- speed 16Gbps
Quad small form-factor pluggable, QSFP
- speed 40Gbps
QSFP+:
- 41.2 Gbps
QSFP28:
- speed: 100 Gbps
QSFP56: 
- speed: 200 Gbps

## Cable Distribution System
---
Demarcation Point
- Location in which the the ISP ends and your LAN begins 
- your lan --> backbone --> edge switches 
	- edge switch is closer to you end user
- minimize cables that have to run veritically 
	- only run MDF to IDF
	- 
66 blocks are for old analog phone lines
110 block is cat 10 americatn termination for high speed networks
	- punch down blocks use punch down tools to hold wires in place 
	- most common used in networks
Krone block analogous to 110 block but  ised mostly in europe
bix block 

## wiring a network
