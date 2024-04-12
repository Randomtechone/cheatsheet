# Nmap Cheat Sheet

## Target Specification

- **Scan a single IP**:

nmap 192.168.1.1


- **Scan specific IPs**:

nmap 192.168.1.1 192.168.2.1


- **Scan a range**:

nmap 192.168.1.1-254


- **Scan a domain**:

nmap scanme.nmap.org


- **Scan targets from a file**:

nmap -iL targets.txt


## Nmap Scan Techniques

- **TCP SYN port scan (Default)**:

nmap 192.168.1.1 -sS


- **TCP connect port scan (Default without root privilege)**:

nmap 192.168.1.1 -sT


- **UDP port scan**:

nmap 192.168.1.1 -sU


- **TCP ACK port scan**:

nmap 192.168.1.1 -sA


- **TCP Window port scan**:

nmap 192.168.1.1 -sW


## Host Discovery

- **List targets only (No Scan)**:

nmap 192.168.1.1-3 -sL


- **Disable port scanning. Host discovery only**:

nmap 192.168.1.1/24 -sn


- **Disable host discovery. Port scan only**:

nmap 192.168.1.1-5 -Pn


- **TCP SYN discovery on port x (Port 80 by default)**:

nmap 192.168.1.1-5 -PS22-25,80


- **TCP ACK discovery on port x (Port 80 by default)**:

nmap 192.168.1.1-5 -PA22-25,80


- **UDP discovery on port x (Port 40125 by default)**:

nmap 192.168.1.1-5 -PU53


- **ARP discovery on local network**:

nmap 192.168.1.1-1/24 -PR


- **Never do DNS resolution**:

nmap 192.168.1.1 -n

## Enumeration

- **SSL enumeration**:
  
nmap X.X.X.X --script ssl-enum-ciphers -p 443  
nmap X.X.X.X --script ssl-cert -p 443
  
- **SSH enumeration**:
  
nmap X.X.X.X --script ssh2-enum-algos -p 22
  
- **Redis enumeration**:
  
nmap X.X.X.X --script redis-info -p 6379
