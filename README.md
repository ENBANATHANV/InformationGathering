# InformationGathering
Information Gathering Techiques

# To perform information gathering techniques

# AIM:

To perform information gathering techniques using kali linux 

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:
Open terminal/browser and try execute necessary commands/use url to perform information gathering

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified for information gathering:

Footprinting is a part of the reconnaissance process which is used for gathering possible information about a target computer system or network.
http://www.whois.com/whois website to get detailed information about a domain name information including its owner, its registrar, date of registration, expiry, name server, owner's contact information, etc.

## OUTPUT:
<img width="1919" height="1028" alt="Screenshot 2026-01-30 091125" src="https://github.com/user-attachments/assets/ff558403-3381-4357-8fae-9b242eab74fc" />


## Finding IP address:
ping command is available on Windows as well as on Linux OS. Following is the example to find out the IP address of facebook.com.
## output
<img width="625" height="533" alt="Screenshot 2026-01-30 091446" src="https://github.com/user-attachments/assets/ca714823-e2c3-425f-943b-07dabd846767" />

### Ping Command

Definition:
Ping is a network utility used to test the connectivity between two devices on a network. It checks whether a host (computer/server) is reachable and measures the time taken for data to travel to the destination and back.

### Purpose of Ping
Checks if a host is reachable
Measures network latency (response time)
Troubleshoots network issues

## Finding Hosting Company
get further detail by using ip2location.com website.
## output
<img width="1919" height="1023" alt="Screenshot 2026-01-30 091854" src="https://github.com/user-attachments/assets/8006de1f-d105-461e-8775-1258250836b2" />



## History of the website:
## output
https://web.archive.org/
<img width="1919" height="1025" alt="Screenshot 2026-01-30 092044" src="https://github.com/user-attachments/assets/15fa672f-7dca-42e4-96ee-f6f3980b73ab" />



# Webserver Fingerprinting:

## Netcat:
sudo nc example.com 80
GET / HTTP/1.1
Host: example.com
<img width="849" height="884" alt="Screenshot 2026-01-30 093409" src="https://github.com/user-attachments/assets/ce5c97c9-7c28-40da-bdfd-9049ffadfa4c" />

### Netcat (nc)

Definition:
Netcat (often called nc) is a powerful networking utility used to read and write data across network connections using TCP or UDP. It is commonly known as the “Swiss Army knife” of networking because of its wide range of uses in cybersecurity and system administration.

### Purpose of Netcat
Test and debug network connections
Scan open ports
Transfer files between systems
Create simple client-server communication
Set up reverse or bind shells (in penetration testing)

### How It Works

Netcat can act as both a client and a server. It establishes a connection to a specified port and allows direct communication between systems.


## nmap:
### output

<img width="911" height="705" alt="Screenshot 2026-01-30 094005" src="https://github.com/user-attachments/assets/d66eb5e1-6990-4dad-84ae-42074788a6e5" />

### Nmap (Network Mapper)

Definition:
Nmap (Network Mapper) is an open-source network scanning tool used to discover hosts, detect open ports, and identify services running on a network. It is widely used in cybersecurity for network exploration and security auditing.

### Purpose of Nmap
Discover devices on a network
Identify open ports
Detect running services and versions
Find security vulnerabilities
Perform network mapping

### How It Works

Nmap sends specially crafted packets to a target system and analyzes the responses. Based on these responses, it determines which ports are open, closed, or filtered, and what services are running.

## Whatweb
### output
<img width="1247" height="560" alt="Screenshot 2026-01-30 094135" src="https://github.com/user-attachments/assets/d11caef0-1c37-4a5a-8cea-4cf42bea03cf" />

### WhatWeb

Definition:
WhatWeb is a web technology identification tool used to detect the technologies used by a website. It helps identify information such as the web server, content management system (CMS), frameworks, and programming languages used in a target website.

### Purpose of WhatWeb
Identifies technologies used by a website
Detects CMS (like WordPress, Joomla)
Finds server information
Helps in web reconnaissance
Assists in vulnerability assessment

### How It Works

WhatWeb sends HTTP requests to a target website and analyzes the responses (headers, cookies, HTML content) to determine the technologies running on the server.

# Tracing the Location
TCP Traceroute:
sudo traceroute -T ikea.com
## output
<img width="764" height="892" alt="Screenshot 2026-01-30 094553" src="https://github.com/user-attachments/assets/f7a178c9-9632-4c9a-8483-ebb1ad245fe8" />
### TCP Traceroute

Definition:
TCP Traceroute is a network diagnostic technique used to trace the path (route) that TCP packets take from a source system to a destination host. Unlike traditional traceroute, which uses ICMP or UDP, TCP Traceroute uses TCP packets—usually directed to a specific port like 80 (HTTP) or 443 (HTTPS).

### Purpose of TCP Traceroute
Identifies the path taken by packets across networks
Detects network delays and bottlenecks
Bypasses firewalls that block ICMP/UDP
Troubleshoots connectivity issues

### How It Works

TCP Traceroute sends TCP packets with increasing TTL (Time To Live) values. Each router along the path decreases the TTL by 1. When TTL reaches zero, the router sends back a response, revealing its identity. This process continues until the destination is reached.

## UDP Traceroute:
sudo traceroute -U ikea.com
## output
<img width="764" height="892" alt="Screenshot 2026-01-30 094553" src="https://github.com/user-attachments/assets/072b489f-3f55-4612-875d-c067a33fac75" />
### UDP Traceroute

Definition:
UDP Traceroute is a network diagnostic technique used to trace the path that packets take from a source system to a destination host using UDP (User Datagram Protocol). It is the default method used by the traditional traceroute tool in many systems.

### Purpose of UDP Traceroute
Identifies the route taken by packets
Detects network delays and failures
Helps in troubleshooting connectivity issues
Maps intermediate routers between source and destination

### How It Works

UDP Traceroute sends UDP packets with increasing TTL (Time To Live) values to high, unused port numbers. Each router decreases the TTL by 1, and when it reaches zero, the router sends an ICMP Time Exceeded message back. When the packet reaches the destination, the host replies with an ICMP Port Unreachable message, indicating the end of the trace.


## ICMP Traceroute:
sudo traceroute  ikea.com
## output
<img width="692" height="827" alt="Screenshot 2026-01-30 094410" src="https://github.com/user-attachments/assets/0b144e34-0bd2-4538-8b7e-5b094b76e508" />

### ICMP Traceroute

Definition:
ICMP Traceroute is a network diagnostic technique used to trace the path that packets take from a source system to a destination host using ICMP (Internet Control Message Protocol) Echo Request messages. It is commonly used in systems like Windows.

### Purpose of ICMP Traceroute
Identifies the route taken by packets
Detects network delays and packet loss
Helps troubleshoot connectivity issues
Maps intermediate routers between source and destination

### How It Works

ICMP Traceroute sends ICMP Echo Request packets with increasing TTL (Time To Live) values. Each router decreases the TTL by 1, and when it reaches zero, the router returns an ICMP Time Exceeded message. This reveals each hop along the path. When the packet reaches the destination, it replies with an ICMP Echo Reply, completing the trace.




## RESULT:
The information gathering techniques tools/procedure were  identified successfully
