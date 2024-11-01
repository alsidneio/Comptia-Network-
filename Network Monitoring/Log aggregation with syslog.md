- syslog is a  protocol used to send system log or event messages to a central server, called syslog server
	- these logs can be sent to: 
		- Security information management , SIM, server
		- Security Event Management , SEM, server 
		- Security Infomation and Event Management , SEIM, server
	- doing this allows the admin to normalize and correlate data
	- client: device sending the syslog 
	- server: receiver of logs 
	- uses port 514 using UDP 

#### Syslog severity levels 
---
0. emergency condition: system has become unstable 
1. alert condition: condition should be corrected immediately 
2. critical condition: a failure in the sustems primary application requires immediate attention 
3. error condition: something is preventing proper system function 
4. warning condition: An error will occur if action is not taken soon 
5. Notice condition: the events are unusual 
6. information condition: normal operational message that requires no action 
7. debugging: useful information for developers 

#### Syslog types
---
Network logs
- Trafic logs: information about traffic flows within your network 
	- traffic logs allow for nvestigation of any abonormalities 

- Audit log: logs that contain a sequence of events for a particular activity 

Windows logs: 
- application logs
	- contains information about the software running on your host
	- app log levels: 
		- Informational 
		- Warning 
		- Error
- security logs: contains information about the security of a host
	- 
- system logs
	- contains information about the operating system itself 
	- system log levels: 
		- informational 
		- warning 
		- error
