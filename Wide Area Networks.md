## Wired WAN connections
---
3 main types: 
	- Dedicated leased line
		- logical connection that connects two sites through a service providers facility or a telephone companys central office 
		- this is a more expensive connection cause its a dedicated line, bandwidth isnt shared with any other customer 
		- 
	- Circuit Switched Connections 
		- connection that works by only being brought up when needed 
		- same connection type as a phone call 
		- dialups and ISDN 
	- Packet Switched Connections 
		- works like an always on dedicated lease line m, but the bandwidth is shared 
		- this option uses SLAs 
		- buit as virtual circuits , which are represented as dashed lines on a diagram 

Physical connections : 
- cpper wire 
	- UTP, STP , COax
		- supports analog and digital connections 
		- dialup , ISDN , E1, D1
- Fiber Optic
	- expensive
	- not suseptible to emf connections 
- Powerlines
	-  Broadband ove Powelines BPL
	- up to 2.7 MBPS
	- allowed widespread connection especially to rural areas                                                                                                                                                                                                                                                                                                                                                                                                                                                 


## Wireless WAN Connections
---
#### Cellular connections 
---
3G has a few different implementation types
- Wideband Code Division Multiple Access, WMCDA
	- uses the UMTS standard 
	- reacches the 2 Mbps
	- its the slowest type 
- High Speed Packet Access , HSPA
	- reaches speeds of 14.4 Mbps
	- refferred to as 3.5G
- HSPA+
	- reaches speed of 50 Mbps 
	- referred to as 3.5G
- 
4G technologies: 
- 4G Long Term Evolution, LTE
- LTE- Advanced, LTE-A
	- 2-3 faster than LTE

5G has banded frequencies 
- low band 
	- 600-850MHz
	- 20-350 Mbps
- Middle Band: 
	- 2.5-3,7 GHz 
	- \100-900 Mbps
	- most carries use this cause of the speed and coverage advantage
- High Band: 
	- 25-39GHz 
	- upwards of Gbps 
	- used where peoople will be gathered communally such as sports stadiums 

Cellular impelemtations
GSM:  Global system for Mobile communications 
	-  takes an analog signal converts it to digital  passses it through the cellular network 
	- given a channel and a timeslot 
	- much more widely supported accross the globe
CDMA:  Code division multiple access
- uses code to split up the channel 
- the channel generally has a code that the other end can pick up 


| Technology | Frequency | speed            |
| ---------- | --------- | ---------------- |
| 1G         | 30Khz     | 2kbps            |
| 2G         | 1800MHz   | 14.4-64 Kbps     |
| 3G         | 1.5-2GHz  | 144 Kbps - 2Mbps |
| 4G         | 2-8 GHz   | 1--Mbps - 1Gps   |
| 5G         | low       |                  |

#### Microwave Connections 
---
Microwave connections us a beam of radio waves in the microwave frequency to transmit information between two fixed locations 

- frequency range: 300MHz - 300GHz
	- Ultra High Frequency, UHF
	- Super High Frequency, SHF
	- Extremely High Frequency, EHF
- Microwave attennas must have line of sight to work 
- Line of sight creates distance limitations 
- Microwave connections were marketed as: Worldwide Interoperability for Microwave Access,  WiMAX 
	- 802.6e standard 

#### Satellite Connections
---
you can get satellite connection anywhere
- good for remote areas 
- best case is for mobile users on the go , not in a localized area

speeds are not as fast as cable of fiber model 
there is a latency in transmisison because of the roundtrips 
its still more costly option for ISPs



## WAN Technologies
---
#### Dedicated Leased Line 
	- singular point to point connection  for your use only , all the bandwidth is yours
	- T1s & E1s  are dedicated/digital circuits are measured in 64 kbps channels , Digital Signal 0(DS0)
	- for leased lines you get a modem looking device, Channel Service Unit/ Data Service Unit(csu/dsu)
		- CSU/DSU teminates the digital signal at the customers location


Digital Signal Levels

| Carrier | Signal Level | # of T1 signals | # of Voice Channels | Speed        |
| ------- | ------------ | --------------- | ------------------- | ------------ |
| T1      | DS1          | 1               | 24                  | 1.544 Mbps   |
| T1c     | DS1c         | 2               | 48                  | 3.152 Mbps   |
| T2      | DS2          | 4               | 96                  | 6.312 Mbps   |
| T3      | DS3          | 28              | 672                 | 44.736 Mbps  |
| T4      | DS4          | 168             | 4032                | 274.760 Mbps |
| E1      | n/a          | n/a             | 30                  | 2.0 Mbps     |
| E3      | n/a          | n/a             | n/a                 | 34.4 Mbps    |
Metro Ethernet
- the replacement for T1,t3
- its cheaper and easier
- its an Rj45

#### Point to Point Protocol, PPP
- its a layer 2 protocol used on top of a dedicated leased line
- used to transmit layer 3 protocals
- Protocal types: 
	- Multilink Interface: 
		- binding multiple devices of the same type and using it as one logical interface
	- Looped Link detection
	- Error Detection 
	- Authentication 
		- Password Authetication Protocol, PAP
			- performs one0way auth between client and server
			- this protocol is not encrypted 
		- Challenge Handshake Auth Protocol, CHAP
			- PAP with the TCP 3 way handshake
			- encrypted with the has h
		- MS-CHAP, Microsofts version of CHAP
			- two way auth, client and server authenticate eachother 

#### Point to Point Protocol over Ethernet, PPPoE
- a network protocol for encapsulating PPP frames inside ethernet frames
- 


#### Cable Modems 
use cable tv infrastructure that is mad up of a hybrid fibe-coax(HFC) distribution Network
- run an a standard called DOCSIS
	- Data Over Cable Service Interface Specification
- upstream: 5-42 MHz
- downstream: 50-860 MHz
- Able to transmit and receive over TV Infra

#### Satellite Modems 
Used in remote , rural , or disconnected locations where other connections are not available
- Satellite has low usage cap, streaming not really an option 
- there is a delay in programming because of transmission distance 
- 
#### Plain Old Telephone Service, POTS
runs on public switched telephone network
- know as analog voice service 
- known as dialup connection
- POTS run over a T1 connection

#### Integrated Service Digital Network 
A technology designed  to carry voice or data over Bearer, B , Channels
- D channels, data or delta channels 
- Basic Rate Interface, BRI
	- tied two B channels together to give you 64 Kbps
- Primary Rate Interface, PRI
	- took 23 B channels and a 1 D channel to give 1.472 Mbps

#### Frame Relay 
Creates virtual circuits to connect remote LANs to WANs
- replaced with cable and DSL because of how cheap it was 
- considered a layer 2 technology 

#### Synchronous Optical Network , SONET
Layer 1 technology that uses fiber as its media and has high data rates between 155Mbps - 10Gbps  or more 
- covers distance of 20km to 250km or more 
- can be implemented in a bus or a ring for layer 2 transmission 

#### Data Rates 

| WAN Technology | Typical Available Bandwidth |
| -------------- | --------------------------- |
| Frame Relay    | 56-1.544 Mbps               |
| t1             | 1.544 Mbps                  |
| t3             | 44.736 Mbps                 |
| e1             | 2.048 Mbps                  |
| e3             | 34.4 Mbps                   |
| atm            | 155 Mbps - 622 Mbps         |
| SONET          | 51.84 Mbps - 159.25 Gbps    |
