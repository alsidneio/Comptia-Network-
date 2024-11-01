## Domain Name System 
---
DNS helps  network clients find a website using human-readable hostnames instead of numeric IP addrs

- A DNS Server does the hostname to IP translation  


#### Fully Qualified Domain Name , FQDN
---

FQDN : a domain name that us under a top level provider(TLP)
	- .com is a tlp
	- example : www.diontraining.com 
		- domain: diontraining.com
		- file server fqdn: ftp.diotraining.com 
		- mail server fqdn: mail.diontraining.com

##### DNS Hierarchy 
- Root
	- answers requests in the root zone 
- Top Level Domain 
	- asnwers requestion in the TPL 
	- example: .com 
- second level Domain 
	- example diotraining.com 
- subdomain 
	- www.diontraining.com
	- support.diontraining.com 
	- mail.diontraining.com
- Host 
	- refers to a specific machine

##### Uniform Resource Locator, URL
contains the FQDN eith the method of accessing information
- securely: use `https://` at the beginning
- non-secure : `http://`
- file servert: `ftp://`

#### DNS Records 
---
CNAME : 
	- resolving one URL to another URL 
	- Application: IF one domain is shutdown, but you still want users to reach some type of content. Use this record for a redirect
	- You cannot point Cname to an IP Addr

MX: 
	- used to route messages that come to the domain over SMTP , Port 25
	- can only be used to point to another domain 
	- there is a priority list on choosing which server to send mail to 
	- same priority creates an alternating, load balanced situation 

SOA: 
	- stores admin information about the domain 
		- when domain was updated 
		- admin email of a domain 
		- important when a zone transfer
	- zone transfer: when one dns transfers its records to another dns 
		- happens over the TCP protocol to ensure recipt of data
PTR: 
	- the opposite of an A record 
	- reverse DNS lookup 
	- lets you lookup a hostname given an IP address 
	- if  PTR record is definded it gets stored as: `<IP_addr>.in-addr.arpa`
		- origins of the internet was: Advanced Research Projects Agency Network, ARPA
		- APRA was the first top level domain defined, used for managing infrastructure
		- 
TXT: 
	- designed to add text to the DNS system , for human readable notes 
	- mostly used to prove domain ownership verification  via machine readable code 
	- 
SRV: 
	-  special because it allows you to specify a port along with a specified IP 
	- 
NS: 
	- Nameserver Record is a type of DNS server that stores all the DNS records for a given domain , the Authority

| DNS Record | Description        | Function                                              |
| ---------- | ------------------ | ----------------------------------------------------- |
| A          | Address            | Links hostname to ipv4 address                        |
| AAAA       | Address            | Links Hostname to ipv6 address                        |
| CNAME      | Canonical Name     | Points a domain to another domain or subdomain        |
| MX         | Mail Exchange      | Directs emails  to a mail server                      |
| SOA        | Start of Authority | Stores Important Information about a domain or a zone |
| PTR        | Pointer            | Correlates an IP address with a domain name           |
| TXT        | Text               | Adds text into the DNS                                |
| SRV        | service            | Specifies a host  and port for a specific service     |
| NS         | NAmeserver         | Indicates which DNS nameserver has the authority      |

Internal DNS
- allows cloud instances on the same network access each other using internal DNS names 