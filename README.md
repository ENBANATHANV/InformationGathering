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



## nmap:
### output

<img width="911" height="705" alt="Screenshot 2026-01-30 094005" src="https://github.com/user-attachments/assets/d66eb5e1-6990-4dad-84ae-42074788a6e5" />

## Whatweb
### output
<img width="1247" height="560" alt="Screenshot 2026-01-30 094135" src="https://github.com/user-attachments/assets/d11caef0-1c37-4a5a-8cea-4cf42bea03cf" />


# Tracing the Location
TCP Traceroute:
sudo traceroute -T ikea.com
## output
<img width="764" height="892" alt="Screenshot 2026-01-30 094553" src="https://github.com/user-attachments/assets/f7a178c9-9632-4c9a-8483-ebb1ad245fe8" />


## UDP Traceroute:
sudo traceroute -U ikea.com
## output
<img width="764" height="892" alt="Screenshot 2026-01-30 094553" src="https://github.com/user-attachments/assets/072b489f-3f55-4612-875d-c067a33fac75" />



## ICMP Traceroute:
sudo traceroute  ikea.com
## output
<img width="692" height="827" alt="Screenshot 2026-01-30 094410" src="https://github.com/user-attachments/assets/0b144e34-0bd2-4538-8b7e-5b094b76e508" />






## RESULT:
The information gathering techniques tools/procedure were  identified successfully
