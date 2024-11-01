#### ipconfig
---
- displays all of the current TCCP?IP network configuration values and refreshes DHCP and DNS settings for a Windows client/server
- dhcp issues
	- release the address : `ipconfig /release`
	- ask for new address: `ipconfig /renew`
		- restarts the DORA process 
	- see all details about tcp/ip config: `ipconfig /all` 
	- restart the computer , 

#### ifconfig, interface configuration 
---
- displays ip  information for \*nix  OS'
- theres no brief version of ifconfig 
	- you can change the number of interfaces returned 
	- all is the default
	- there is a verbose option for specific 
	- shutdown an interface: `ifconfig down`
	- enable an interface: `ifconfig up`
- ifconfig is deprecated and you should be using IP

#### IP
---
- the replacement for ifconfig on \*nix systems 
- assigns an address to a network interface or configures network interface parameters on a \*nix system 
- supports the same functions as `ifconfig`
- 