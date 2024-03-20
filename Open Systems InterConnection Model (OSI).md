PDTSPA
please do not tell shore patrol anything 
physical, data, transport, session, presentation, application  

Data has different names as it moves through the OSI model: 

Layer 5,6,7: Data
Layer 4: segments
Layer 3: packets
Layer 2: frames
Layer 1: Bits
## Layer 1: Physical 
---
- Transmission of bits across the network occur here 
- two standards at this layer to wire networks
	- TIA/EIA-568A 
	- TIA/EIA-568B
	- cross v. straight through
#### Considerations at Physical Layer 
- network physical typology
- synchronized communication
	- Async comms 
	- sync comms
		- have a start and stop bit 
		- use a clock reference 
- How is bandwith going to be used: 
	- broadband: channels using a different portion of the frequency 
	- baseband: use all band at one time  
		- baseband uses a synchronus clock 
		- examples: telephone, ethernet
		- to get more out of the baseband people use time division multiplexing: oeople get specific time slots 
		- theres also stat time division: its dynamic, meaning sis the time slot being used 
		- Freq. division multiplexing. basically makes it broadband. 
Layer 1 devices :  passing stuff along 
	- a cable (media)
	- wifi, bluetooth , 
	- hubs, access points, media converters

## Data Link Layer: Layer 2 
---
Data types: Frames

- Media Access Control (MAC) device
	- MAC address are: hexadecimal 48 bit numbers
	- first 3 are the vendor code
	- second 3 is the unique id 
- Logical Link Control 
	- controls the flow of data between devices 
	- slow down, hold, frame was not recieved, frame was corrupted 
- Synchronouse communication modes: 
	- isochrononus: 
		- Network devices use a common clock source to create time slots for transmissions
	- sychronous: 
		- beginning and end frames with control bits 
		- 

Layer 2 devices: 
- Network Interface cards 
- switches: switches use ports to determine lines of communications 
- bridges 

## Network Layer: Layer 3 
---
Routing/forwarding packets 

Internet Protocol(IP): IPv4/IPv6


#### Concerns at layer 3
1. How to implement packet swithing/routing"
	- packet switching(routing, most common)
		- generaally what people think of in ip routing 
	- cirtcuit switching 
		- a dedicated route (think telephone connection)
	- message switching 
		- wait and route protocol
2. Route discovery and selection
	- static v. dynamic route selection
	- this determine how data is going to flow acrross the network. 
3. Connection Services 
	- provides more flow control to build upon layer 2
	- packet reordering 
	- internet control Message protocol (icmp)
		- the `ping` command
Layer 3 devices: 
- router 
- multilayer switch (smart switch)
- IP

## Transport Layer: Layer 4
---
Data Type: Segmentps

Protocols:
- TCP Transmission Control Protocol 
	- confirmed connection 
	- 3 way handshake: syn --> syn-ack --> ack
	
- UDP: unicast  datagram protocol
	- its a broadcast protocol 
	- its useful for audio and visual streaming 

| TCP                                                       | UDP                            |     |
| --------------------------------------------------------- | ------------------------------ | --- |
| Reliable                                                  | Unreliable                     |     |
| Connection-oriented ( 3 way handshake)                                       | Connectionless (broadcast)                 |     |
| segment retransmission and flow control through windowing | No windowing or retransmission |     |
| Segment sequencing                                        | No Sequencing                  |     |
| Aknowledgements                                           | No Acknowlegments              |     |
|                                                           |                                |     |
Windowing: the time in ehich you can send data , it varies depending on the retransmit signal that it gets from the destination on the destination host

Buffers: storage queue for storing packits on data transmission 
	- when buffer is full dat begins to drop

Load Balancers/firewalls are layer 4 components

## Session Layer: Layer 5
---
session: a diresct connection to a host 

setup a session:
	- Check user credentials 
	- assign a number to session to identify them

Maintain a session: 
	- transferring data back and forth
	- if connection is brokken, try to reconnect
	- Acknowledgement receipts

Tearing down a session: 
	- session tear down, disconnect

#### Devices/Protocol/Software
---
Protocol: 
	- H.323 : used to set up, maintain , and tear down voice and video connections
		- RTP: real time protocol 
		- teleconnections

Software: 
	- NetBIOS: used to share files over a network

Devices: 
	

## Presentation Layer: Layer 6
---
Responsible for data formatting and data encryption

Data is formatted by the computer for destination compatibility
	- ASCII: American Society for Computer Information  Interchange: text based language
		- ensure data is readable
		- Provides proper data structure
		- compouter code 65 == A, code 40 == @
		- Negotiates data transfer syntax for the application Layer
	- jpg, gif, png
	- 
Encryption: obsfuscation of data for securtity as it crosses the network
	- TLS: Transport Layer Security
		- padlock nexct to domain name 

#### Layer 6 examples
---
- Scripting languages
- Standard tex
	- unicode ascii
- puctures
- Movie files 
- encrytption algorithms:
	- TLS
	- SSL

## Application Layer: Layer 7
---
- Responsible for:  
- communication orchestration:  with the computer components for network applications
	- file transfer, email, client/server processes , remote access, network management

- service advertisement: 
	- telling the larger network about the state of the services available 
	- email application 
	- web browsing 
	- domain name servixe 
	- ftp
	- remote access 

## WiresShark : Analyzing network Packets
---

## Encapsulation and Decapsulation
---
Encapusulation: Process of putting headers and trailers around some data
	- this happens as you send data from layer 7 --> 1

Decapsulation: reading data in an encapsulated packet
	-  this happens as you send data from layer 1 --> 7

Protocol Data Unit (PDU):  A single unit of information transmitted in a computer network
	- this protocol is used to send information up/down the OSI layers
	- Layers 1-4 have special names for their PDUs:
		1. Bits
		2. frames
		3. packets
		4. TCP: segments, UDP: Datagrams
As data passes through each layer a header is added 

#### Important Header Layers
---
Layer 4:  Adding Source & destination ports
- TCP Header: 20 bytes total, 11 fields, 10 mandatory:
	- **Source Port**
	- **Destination Port**
	- Sequence # 
	- Acknowledgement # 
	- Offeset
	- Reserved 
	- **TCP Flags**:
		- Synchronization/SYN
		- Acknowledgement/ACK: Successful receipt of packages
		- Finished/FIN: Used to tear down virtual connections
		- Reset/RST: used to tell client its not accepting connections
		- Push/OSH: Used to ensure data is given priority. 
			- Can be at beginning or end of a segment/ processed by sender or receiver
		- Urgent/URG: 
			- like push but processed by the receiver and is put at the front of a segment, process immediately
	- Window
	- Checksum
	- Urgent Pointer
	- mTCP(optional)

- UDP Header: 8 bytes, 4 fields 
	- Source Port
	- Destination Port
	- Length
	- Checksum

Layer 3:  Adding Source and destination IP
- IP Header: 
	- Version 
	- Length
	- type of service 
	- total Length
	- identifier
	- flags
	- fragmented offset
	- time to live 
	- protocol
	- Header Checksum
	- source IP Address
	- Destination IP Address
	- Options and Padding
	- 
Layer 2:  Adding Source and destination MAC addreaa
- Ethernet Header: 
	- Destination MAC address 
	- Source MAC Address
	- EtherType
	- VLAN Tag
- Payloads: 
	- VLAN: 42 bytes min
	- NO VLAN: 46 Bytes min
	- maxc payload sizee MTU == 1500 Bytes
		- if a frame is bigger the 1500 then you need to allow a general frame

Layer 1:  bTransmit Layer to frames as 1s and 0s
