SLAAC is a fundamental component used to simplify the network configuration process and make assigning IP addresses easier 

- slaac allows your device to establish its own ip identity without a central server like a DHCP

#### Benefits
1. ENhance the efficiency of the nerworks
2. eliminate the potential for ip conflicts 
3. streamline the process of intergrating new devices ino the networks

#### PRocess: 6 steps
1. device initiation: as it connects it creates 
2. router solicitation: sends a UDP to any routers for identification 
3. router advertisement: router says hey this is what I know about the network and heres a prefix
4. address configuration: takes the prefix and mac address to create a unique ID
5. final check: make sure I am the only one using this address  
