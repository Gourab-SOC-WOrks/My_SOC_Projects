###### Objective



Identify suspicious DNS behavior and possible beaconing.



##### Filters Used

dns





###### Analysis Performed



Statistics → Conversations → DNS



* Identified repeated queries from same internal IP
* Low packet size and fixed intervals observed





###### Findings

* Internal host repeatedly querying same domain
* Pattern consistent with DNS beaconing
