## Module 13 - Attackers Techniques

### Hacking Preparation
- How hackers gather information about orgs

**Passive Information gathering**
- passive search
- search internet
- helps narrowing down to search for Vulnerabilities.
- learn about people in orgs- actual names, phone numbers, office locations or other information, can be used for social engg attack.
- the more information hacker has, the easier will be the attack.

- several websites can help: - can provide information about the target web server or open ports on public IPs.
  - www.netcraft.com
  - www.shodan.io
  - www.censys.io

**Active Scanning**
- after passive scanning, attacker plans active scanning. it involves some level of actual connection to the target system.
- it is most likely to be detected, but also the most likely to yield actionable information.
- type:
    - **Port Scanning:** scan for well known ports (1024), can tell great deal of information.
    - **Enumeration:** try to find out what is in the network. sharedfolders, useraccounts etc.
    - **Vulnerability assessment:** use tools which seek out known vulnerabilities, manually assess vulnerabilities.

    - tools available free on internet:
       - **Ping scan**: but most firewalls block ICMP.
       - **Connect Scan**: tries to make full connection to target IP on a given port. *unlikely to trigger alarm, as server/firewalls get SYN packets*
       - **FIN SCAN**: this scan has FIN flag. - *unlikely to trigger alarm*
       - Null scan, with no falgs set.
       - XMAS scan, with several flags set.
       - most will leave some trace of the attack in the server/fw logs.


### The Attack Phase
- attacker will be ready to attack, after getting information from passive scanning, port scanning, enumerating and gathering info.

**Physical Access Attacks**
**Bypassing the Password**
**Remote Access Attacks**
  - SQL Injection
  - Cross-Site Scripting (XSS)

### Hacking Wi-Fi
- another target for attack.
- **Jamming** - kind of dos
- **De-authentication** - this is sending a de-authentication or logoff packet to the wireless access point. The packet will spoof the users IP. then trick the user to login through access point.
- **WPS attack** - WPS (Wi-Fi Protected Setup) uses a PIN to connect to Access Point. - attempts to interept that PIN in transmission, connect to the WAP, then steal the WPA2 password.
- **Cracking the password** - a bad wi-fi password can be cracked easily.
