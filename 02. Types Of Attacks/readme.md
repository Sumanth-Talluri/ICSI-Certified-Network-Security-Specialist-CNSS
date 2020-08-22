## Module 2 - Types of Attacks

### 1. Denial of Service Attacks (DoS/DDoS)
- **SYN Flood**
   - uses TCP SYN
   - Attacker sends a number of connection requests very rapidly then does not responds to server responses
   - this leaves connection on server **half** open, reserves buffer memory.
   - usually packet in buffer is dropped (in about 3 mins)

- **Smurf Attack**
   - popular type
   - named after application used first
   - an ICMP packet is sent to broadcast address, but return address is altered/spoofed to match one of the computers on the network.
   - difficulty is to get packets to start on the target network.
   - can be accomplished via some softwares/virus/trojan horse.

- **Ping of Death**
   - PoD, works to compromise systems that cannot deal with extremely large packet sizes (config issues/ vulnerabilities in OS/Apps)
   - make sure all OS/Softwares are patched.
   - less common now, as new OS/Apps handle oversized packets better.

- **UDP Flood**
   - uses UDP, connectionless (no confirmations/acks), allows packets to be sent much faster (easier to perform DoS)
   - UDP Flood attack works when an attacker sends a UDP packet to a random port on the victim's system. When system receives it, it will check which application is waiting on that port. After realizing no application is waiting, it will generate ICMP packet for destination (mostly forged/unreachable). If enough UDP packets are delivered to ports, the system can go down.

- **DoS Tools**
    - LOIC (Low Orbit Ion Cannon)
    - HOIC (High Orbit Ion Cannon)  


### 2. Buffer Overflow attacks
- uses applications (not properly written to handle bigger size buffer).
- oversized buffer can be written to disk.
- attacker can write malicious code with buffer overflow.
- keep OS/Apps uptodate.

### 3. IP Spoofing
- attacker change source ip address (to a trusted system) of packet.
- attacker should know trusted IP of target.
- are becoming less frequent.
- used in DoS.  


**ways to address**
- do not reveal info regarding internal IPs/trusted IPs.
- Monitor incoming packets from outside networks. (using Netlog etc). It checks for incoming packets to see if both source and dest IPs are from internal network. If yes, means attack in underway.

- examples of potentially vulnerable configs
   - Routers (internet) support multiple interfaces
   - Proxy firewalls authenticating using Source IP.
   - Routers which dont filter packets.


### 4. Session Hijacking
- TCP session hijacking - hacker takes over TCP session between two machines.
- this is because authentication is done mostly only at the start of TCP Session.
- **using source-routed IP packets** - MITM.
- The point of hijacking a connection is to exploit trust and gain access into a system.
