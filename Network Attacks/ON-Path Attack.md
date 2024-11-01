- An attack where the attacker or pentester places their workstation between two hosts to captue , maonitor, and relay communications #Network-plus-Definitions 

why: 
	- can intercept authorization packets and take over session 

Attack types: 
1. Replay attack:  occurs when attacker captures valid data and repeats it either immediately or with delay
	- 
2. relay attack: occurs when the attacker is able to insert themselves between two hosts and become part of  the conversation.

On-path attack is weak against encrypted communications
- one method for getting around this is SSL stripping : redirecting Https reqs to Http in an attempt to trick the encryption application 
- another method of aversion is to have the client or server abandon its higher security mode  for a lower security mode. 
	- allowing at a lower level makes it easier to crack the encryption in real time. 