#### DNS Cache Poisoning (DNS Spoofing)
---
- involves corrupting DNS resolver cache with false information to redirect traffic
	- to prevent this use DNSSEC, the dNS security extensions
	- DNSSEC will add a digital signature
#### DNS Amplification Attacl
---
- involves exploiting the DNS resolution process to overwhelm the system with response traffic
- the sender ip is generally spoofed 

to prevent: 
- rate limit dns responses 
#### DNS tunneling 
---
- involves using the DNS protocol in order to encapsulate non-DNS trafffic to bypass firewall rules

#### Domain Hijacking (Domain Theft)
---
involves changing the registration of a domain name without the permission of the original registrant
- can lead to loss of control to a website and redirect to malicious sites

To prevent: 
- conduct regular updates 
- ensure that account registration information is secure
- use domain registry lock services

#### DNS Zone Transfer Attacks
---
- an attack in which the attacker tries to get a copy of the entire DNSzone data by pretending to be an authorized system

why: 
- 
