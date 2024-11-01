Networks have converged so we now have to worry more about efficient use of Bandwitrh 

- QoS enables optimization of nwetwork performance based different types of traffic #Network-plus-Definitions 

Optimization looks like: 
1. categorizing the types of traffic
2. determine how much bandwidth is required, for each type 
3. efficiently use WAN links bandwidth
4. determining the types of traffic to drap during network congestion

- QoS categories
	1.  delay
		- time it takes for data to travel from source to destination 
	2. jitter
		- uneven, unorded arrival of packets
		- generally bad for voip and video
	1. drops
		- In congestion packets will get dropped 
		- in UDP situations there are no resends

# Qos Categorization (methods of traffic handling  )
---
Higher prioty gets to use bandwidth during congestion 

1. best effort: first in first outr 
2. integratied services, Hard Qos: 
	1. traffic has strict bandwith reservations
3. differentiated services, soft Qos: 
	1. the bandwidth reservation are a suggestion
	2. some flexibiliyt built in how much each traffic type gets 

# QoS Mechanisms (How we determine priority)
---
