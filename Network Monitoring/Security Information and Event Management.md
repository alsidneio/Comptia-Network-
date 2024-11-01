- SIEM: a tool that provides real-time or near-real-time analysis of security alerts that are generated 
- security relies on reviewing: 
	- logs 
	- informational alerts 
	- events
- Log reviews should be done regularly 
- SIEM does correlation of events accross devices 
- SIEM works on port:
	- 514 via UDP
	- 1468 via TCP

#### SIEM Method for event correlation 
---
Log collection: 
- provides import forensic tools and helps address compliance reporting requirements
Normalization: 
- Maps log messages into a common data model, enabling the organization to connect and analyze related events
Correlation: 
- Links logs and events from different systems or application into a single data feed for faster response/analysis
Aggregation: 
- reduces the volume of event data by consolidating duplicate event records and merging them into a single record
Reporting: 
- Presents the correlated, aggregated event data in real time monitoring dashboards for analyst or summaries for management

#### SIEM Implementation methods 
---
as software on a server
as hardware device 
As a remote managed service 

#### SEIM Deployment considerations
----
1. Log relevant events and filter out irrelevant 
2. Establish and document the scope of the events 
3. develop use cases to define a threat
4. plan inscident response for scenarios and events 
5. establish ticketing process to track all flagged events
6. Schedule regular threat hunting with cyber ssec analyst
7. provide auditors an evidence trail 

