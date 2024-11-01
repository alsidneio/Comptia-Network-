ACL is a list of permissions associated with a given system or network resource
- acl can be applied to any packet filtering device
- acl can be applied based on port, IP, or application

- acl is a top down read, Specific at the top, generic rules at the bottom

Things you may want to block using an ACL
- Block requestss from internal or private loopback addrasses and multicast IP ranges
	- 192.x.x
- Block incoming request from protocols that should only be used locally 
	- icmp, dhcp, ospf , smb
- Block all IPv6 traffic or allow it only to authorized ports and hosts

#### ACL structure
---
list name
remark: details about the list
permit means allow 

`<permission> <protocol> <mask> <port><restriction > <function>`
`permit tcp 10.0.2.0 0.0.0.255  eq 443 any established`

note: www = = port 80, domain == port 53

Explicit deny: blocks any matching traffic
implicit deny: 