###### Objective



Inspect HTTP traffic for malicious indicators.



###### 

###### Filters Used

http.request





###### Analysis Steps



Statistics → Conversations → TCP



Follow → HTTP Stream



###### 

###### Findings



* Repeated HTTP GET requests
* Suspicious User-Agent string
* Non-browser-like behavior
