Authgentication: the process of determining wherher someone or something is who or what it claims itself to be

Local authenticat5ion
	- username and password

LDAP: lightweight Directory Access protocol #Network-plus-Definitions 
	- a DB that is used to centralize information about the clients and the objects on the netrwork
	- simplified version of X.500
	- uses port 389
	-  LDAP secure uses port 636
	- used to validate password AND USERNAME COMBINATION
	- Microsofts version of LDAP is call Active Directory
		- AD organizes and manages everything on the network including clietns, servers , devices and users

Kerberos: 
- authentication and authorizastion within a windows environment
- provides two way or mutal authentication
- tuns on port 88
-  single point of failure  becuase of the resources server 

SSO
- linking a default profile to multiple sites needed to log in 
- if credentials get compromised, attacker will have access to all resources that the profile has access to

SAML: security assertion Markup Language #Network-plus-Definitions 
- xml based data format that is used to exchange authentication information between a client and a service
- Generally paired with SOAP, Simple Object Acces Protocol for authorization as well
- Three main roles in SAML: 
	- Service Provider
	- User Agent : generally the browswer 
	- Identity Provider
	- 

RADIUS: Remote Authentication Dial-In user Service #Network-plus-Definitions 
- provides centralized administration of dial-up, VPN and wireless authentication so it can be used with both 802.1x and Extensible Authentication Protocol
- this protocol is cross platform

TACACS+ : Terminal Access Controller Access control System Plus
- developed byy cisco and it can perfome the role of authenticator in an 802.1x network
- tacas is a bit slower because it uses TCP 
- supports all protocols 
- needs to use all cisco products in your network 

Time based authentication
- time based one time password 
- 