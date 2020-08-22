## Module 1 - Introduction to Network Security

### Basics
- ipv4, ipv6
- dns
- ports
- TCP/IP

### Analyzing Network Traffic
- using wireshark
    - analyze web Traffic
    - analyze Telnet Traffic (un-encrypted, can see all user/pwds)

### Basic Network utils
- ping (ICMP)
- netstat (netstat -tulpn)
- tracert(traceroute)
- ipconfig/ip/ifconfig


### OSI Model
- Application (POP,SMTP,FTP,HTTP)
- Presentation (NDR,LPP)
- Session (NetBIOS)
- Transport (TCP/UDP)
- Network (Routes, IP/ARP/ICMP)
- Data Link (MAC/LLC)
- Physical (cable/nic)



### Thread Classification
Three types - categorized attacks based on what they actually do
- Intrusion
   - hacking and cracking.
   - using security flaws in OS/app, using security misconfigurations.
   - social engg, war driving to hack wireless networks.

- Blocking/DoS
   - DDoS


- Malware
  - most common threat to any systems.
  - designed to spread on their own
  - wildly spread
  - example - virus - replicate and spread  
      - can spread using addressbook/emails  
      - can cause networkshutdowns/heavy network Traffic  
  - Trojan horse
      - secretly downloads a virus or malware.  
      - more likely to be found in illegitimate softwares or pirated copies of softwares.  
  - Spywares
      - increasing at pace
      - spies on computer
      - can track web-cookies, files etc
  - keyloggers


### Security Terminology
- Firewall
- Proxy Server
- IDS
- Access Control
    - Authentication
- Non-Repudiation
- Least privilege
- CIA Triad (Confidentiality, Integrity, Availability)
    - Confidentiality: drive encryption, good passwords, MFA
    - Integrity: digital signature
    - Availability: backup/HA

- Hackers:
    - White Hat Hackers
    - Black Hat Hackers
    - Grey Hat Hackers


### Approaches of Network Security
- Perimeter Security Approach
- Layered Security Approach
- Hybrid Security Approach
