A digitsl certificate is a digitally signed electronic document that binds a public key with a users identity

- uses the x.509 protocal  in the PKI 

wildcard certificate
- allows all of the subdomains to use the same public key certificate and have it displayed as valid

Subject Alternate Name field 
- certificat that specifies what additional domains and ip Addresses are going t6o be supported 

Single sided certificate: 
- only requries the server to be validated 
- only one side of authentication 

dual sided certificate 
- requires client and server to be authenticated
- requires more processing power, designed for high security environments

self signed certificates
- digital cert that is signed by the same entity whose identiy it cerifies 
- low trust systems or where systems are already trusted

third party certs 
- digital certs issued by a trusted CA
- CA os third party issueing digital certs 

root of trust
- each certificates is validated using the concept of a root of trust/ chain of trust

Registration Authority
- to get a certificiate for your site , you have to buy an RA
- an RA requests identifying information from the user and forwards that cereticate request up to the CA to create a Digital CERT

Certificate Signing request 
- is a block of encoded text that contains information about the entitry requesting the  certificate