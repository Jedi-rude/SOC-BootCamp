# SOC-BootCamp
Basic SIEM Integration and SOC Monitoring

##  BootCamp Diagram

<p align="center"><img src="https://github.com/user-attachments/assets/83b4c3dd-c981-4659-a263-3db610e08e15"><br> Project Diagram</p>


##  BootCamp Objectives
This bootcamp help to understand what are the basic operation for the Security Operation Center Monitoring (SOC) operations and basic security integration engineering concepts.


##  Description

This is integration system between SIEM, XDR and Vulnerability scanner (Nessus) to detect seameless visibility and vulnerbilities within system.


##  Prerequsite for this lab

Platforms 
- Windows Server
- Windows Workstation
- Linux Server
- Linux Client
- Nessus Vulnerability Scanner
- SIEM (QRadar, Elsaticsearch, Splunk)
- XDR (Trend Vision One)


##  Details

There are four main security components which are SIEM, XDR, Nessus, and Service Gateway. 


###  SIEM (Security Information and Event Management)

- The SIEM platform includes Elastic and Splunk, which are commonly used for collecting, analyzing, and visualizing security events and logs.
- The SIEM receives log data from the network and systems, helping to detect, investigate, and respond to security threats.

###  Trend Micro

- Trend Micro appears to be the central anti-malware or endpoint security solution. It connects with various endpoints, possibly for managing and protecting them from malware and other threats.
- The Trend Micro XDR cloud communicates with the Service Gateway and directly with the servers and endpoints in the network.


###  Service Gateway

- This acts as an intermediary or connection point for various components, facilitating secure communication.
- The Service Gateway links with Trend Micro, the Nessus vulnerability scanner, and other network elements to allow data exchange, commands, and security updates.


###  Nessus Vulnerability Scanner

- Nessus is responsible for scanning the network for vulnerabilities. It sends vulnerability reports to Trend Micro or the Service Gateway, which could then correlate the information with SIEM or Trend Micro’s threat management.
- This ensures vulnerabilities are tracked and managed across systems.


###  Endpoints/Servers

- The network includes various servers and operating systems, such as Oracle Linux 8, Red Hat 8, SUSE 12, and Windows Server 2016.
- These endpoints are protected by Trend Micro, which scans them for malware and other security risks.
- They are part of a managed security ecosystem, where vulnerabilities are scanned (by Nessus), threats are managed (by Trend Micro), and logs are sent to the SIEM for analysis.


###  Flow

- Red Dotted Line: Indicates communication from the endpoints to Trend Micro for threat protection.
- Blue Dotted Line: Indicates communication for data exchange, vulnerability, or security event information between components, such as from Trend Micro to the SIEM or Service Gateway to Nessus.
