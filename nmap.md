# Nmap Cheat Sheet

## Target Specification

- **Ways to Scan**:

```nmap 192.168.1.1```  
```nmap 192.168.1.1 192.168.2.1```  
```nmap 192.168.1.1-254```  
```nmap 192.168.1.0/24```  

- **Scan a domain**:

```nmap scanme.nmap.org```


- **Scan targets from a file**:

```nmap -iL targets.txt```


## Nmap Scan Techniques

- **Fast scan**:

```nmap -T4 192.168.1.1```

- **TCP SYN port scan (Default)**:

```nmap -sS 192.168.1.1```


- **TCP connect port scan (Default without root privilege)**:

```nmap -sT 192.168.1.1```


- **UDP port scan**:

```nmap -sU 192.168.1.1```


- **TCP ACK port scan**:

```nmap -sA 192.168.1.1```


- **TCP Window port scan**:

```nmap -sW 192.168.1.1```


## Host Discovery

- **List targets only (No Scan)**:

```nmap -sL 192.168.1.1-3```


- **Disable port scanning. Host discovery only**:

```nmap -sn 192.168.1.1/24```


- **Disable host discovery. Port scan only**:

```nmap -Pn 192.168.1.1-5```


- **TCP SYN discovery on port x (Port 80 by default)**:

```nmap -PS22-25,80 192.168.1.1-5```


- **TCP ACK discovery on port x (Port 80 by default)**:

```nmap -PA22-25,80 192.168.1.1-5```


- **UDP discovery on port x (Port 40125 by default)**:

```nmap -PU53 192.168.1.1-5```


- **ARP discovery on local network**:

```nmap -PR 192.168.1.1-1/24```


- **Never do DNS resolution**:

```nmap -n 192.168.1.1```

## Enumeration

- **SSL enumeration**:
  
```nmap --script ssl-enum-ciphers -p 443 192.168.1.1```   
```nmap --script ssl-cert -p 443 192.168.1.1```   
```nmap --script http-security-headers -p 443 192.168.1.1```
  
- **SSH enumeration**:
  
```nmap --script ssh2-enum-algos -p 22 192.168.1.1```   
  
- **Redis enumeration**:
  
```nmap --script redis-info -p 6379 192.168.1.1```   
