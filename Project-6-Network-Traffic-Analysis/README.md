🔹 Project Overview



This project focuses on network traffic analysis using PCAP files to identify suspicious communication patterns that may indicate malware activity. Using Wireshark, DNS queries, HTTP requests, beaconing behavior, and suspicious IP communications were analyzed and mapped to the MITRE ATT\&CK framework.



This project simulates real-world SOC Level 1 / Blue Team analysis using offline packet captures.



🎯 Objectives



* Analyze PCAP files using Wireshark
* Inspect DNS and HTTP traffic
* Identify beaconing behavior
* Detect suspicious IP addresses
* Map findings to MITRE ATT\&CK techniques



🛠 Tools \& Technologies



1. Wireshark
2. Kali Linux
3. PCAP datasets (You Dirty RAT Pack)
4. MITRE ATT\&CK Framework



📁 Project Structure

Project-6-Network-Traffic-Analysis/

│

├── 1\_PCAP\_Files/

│   ├── malware\_sample.pcap

│   ├── dns\_beaconing\_sample.pcap

│

├── 2\_Tools/

│   ├── Wireshark\_Setup.md

│

├── 3\_Analysis/

│   ├── DNS\_Analysis.md

│   ├── HTTP\_Analysis.md

│   ├── Beaconing\_Detection.md

│   ├── Suspicious\_IPs.md

│

├── 4\_Detections/

│   ├── Detection\_Logic.md

│   ├── Wireshark\_Filters.txt

│

├── 5\_Evidence/

│   ├── dns\_queries.png

│   ├── http\_requests.png

│   ├── beaconing\_graph.png

│

├── 6\_MITRE\_ATTCK/

│   ├── MITRE\_Mapping.md

│

├── 7\_Report/

│   ├── Network\_Traffic\_Analysis\_Report.pdf

│

└── README.md



📸 Screenshots Included



* DNS query volume and spikes
* HTTP request patterns
* I/O Graph showing beaconing
* Endpoints and Conversations statistics
