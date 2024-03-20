- This model has 4 layers and is how the modern world generally works 
- TCP v. OSI model: 
	- application, presentation, session layers == Application  layer in tcp 
	- transport == transport 
	- network == internet 
	- data link, physical == Network interface model 

#### TCP/IP Layers 
---
1. Network Interface Layer: 
	1. This layer describes thow to transmit bits across a network and determines how the network medium is going to be used 
2. Internet layer: 
	1. This layer determines where data is taken and is packaged into IP datagrams
	2. examples: IP,icmp , arp, reverse ARP
3. Transport Layer:
	1. defineces the service/proptocal being used 
4. Application layer 
	1. determines how the programs are going to interface with the transport layer
	2. examples: http snmp telsnet ftp smtp ssl/tls ssh

### Data Transport ver networks
---
port: logical opening thats listening or waiting for traffic 
ports are numbered 0-65535

reservered ports: 0-1023
ephemeral ports: 1024 to 65535

- ipv4 packets have: 
	- source address
	- destination address
	- ip flags
	- protocol  type

### Ports & Protocols 
---
protocol, 

#### Reserved Ports
---

- File transfer protocol:
	- port 20/21
	- Provides insecure file transfer
- Secure Shell (SSH): 
	- Port: 22
	- Provides secure remote control of a remote device , using a terminal environment 
- SFTP Secure file transfer protocol
	- port: 22
	- provides secure file transffer
- Telnet 
	- port 23 
	- proved insecure remote control of a terminal based enornment 
- Simple mail transfer protocol SMTP
	- port: 25
	- provides to send abitlity to send email
- Domain Name Service
	- Port: 53
	- sonverts domain names to IP adddresse and vice versa 
- Dynamic Host control Protocol  DHCP: 
	- Port: 67/68
	- Provides network params to your clients such as the ip address subnet gateway and the dns server they should be using 
- Trivial FIle Transfer Protocol 
	- Port: 69 
	- used as a lighteright file transdfer method for sending files or neteork booting of an operating system 
- Hypertext transfer porotocoal:
	- port 80 
	- used for insecure wev browsing 
- post oddice protocal v3 POP3
	- port 110
	- used for incoming emails
		- cant maintain read/unread states 
- Network Time Protocol 
	- port 123
	- used to keep accurate time for clients on a network 
- Network Basic input/output System (Net BIOS )
	- port: 139
	- used in file or printer sharing in windows network
- Internet Mail Application Protocal IMAP
	- port 143 
	- A new method of retrieving  incomeing  email which improves POP2 protocol
- Simple Network Management Protocol SNMP
	- ports: 161 162 
	- used to collect datat about network devicaes and monitor status 
- Lightweight Directory Access Protocol LDAP 
	- port 389
	- used to provide directory service to your network
- HTTPS: 
	- port 443 
	- a secure http using ssl or tls 
- Server Message Block protocal 
	- port: 445 
	- used for windows file an printer sharing services
- System logging protocel 
	- port 514
	- used to send logging data back to a centralized server 
- Simple Mail Transfer Protocol  Transport Layer Securtiy  SMTP TLS 
	- port 587
	- sam as SMTP but encrypted
- Lightweight Directory Access Protocol secure LDAPS
	- port 636
	- LDAP but secure
- Inter message Access Protocol over SSL 
	- port 993
	- IMAP but secure way to send and receives email
- POP3 over SSL
	- port: 995
	- POP3 but secure 

#### Ephemoral Ports
---
- Structered Query language Server Protocal SQL 
	- port: 1433
	- used for communication from client to server SQL DBs
- SQLnet Protocol
	- port 1521
	- used to communicate from a client to an oracle datatbase
- MYSQL
	- prot 3306
	- used for communication from a client to the mysql database engine
- Remote desktop Protocol RDP
	- Port: 3389
	- Provides graphical remote control to a server 
- session initiation protocol SIP
	- ports: 5060, 5061
	- used to initiate voip and video calls. 

## Finding Open Ports
---
- tool: NMAP: network mapper 

```shell

	nmap -sS -O <ip_address> | more 

# -sS: only look for the syn packets 
# -O: show the operating system

```

tool:  zenmap: graphical interface for nmap , shows topology. 

## IP Protocol Types 
---
- Transport Commision Protocol (TCP)
	- trabsfer protocol for the reliable transmission of packets
	- uses threee way handshake to initiate connections 
	- how uch data is sent is negotiated through windowing
	- considered a connection oriented method of communication 

- User Datagram Protocol, UDP
	- an unreliable way to transmit packets
	- connectionless method of communication 
	- can only check if data is corrupted through a checksum

- Internet control message protocol, ICMP
	- used to communicate network connectivity state back to the sender
	- icmp is protocol number 1 in the TCP suite 
	- used as an error reporting and query service

- Generic Routing Encapsulation 
	- used as a simpe way to create a GRE  tunnel over a public network
	- This type of tunnel is not seccure
	- at the router level you need to set the max byte size

- Internet Protocol Security, IPSec
	- used to protect one or more data flows between peers, via encryption
	- IPSec is a TCP protocol
	- IPSec Ensures: 
		- Data Confidentiality , integrity, origin authentication , anti-replay
	- to ensure encryptoion IPSec uses: 
		- Authentication Headers, AH: Integfrity and authentication
		- Encapsulation Security Payload, ESP

NOTE: MAKE NOTECARDS FOR THE PROTOCAL TYPES