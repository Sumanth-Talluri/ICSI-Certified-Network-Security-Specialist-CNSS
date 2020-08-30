## Module 8 - Virus Attacks and How to Defend

### Virus Types and Attacks.
- **What is a Virus** - self-replicates and spreads.
- **What is a Worm** - special type of virus, can spread without human intervention. Most of the virus today are worm.

- **How a Virus Spreads**
    - two ways   
        1. most common and simplest, reads email address book and emails itself to everyone in the addressbook.    
        2. scans for network connections then copy itself to other machines.
    - it can potentially delete files, change sys settings or harm the system any way possible.

**some examples**

- **Rombertik**
    - 2015, malware uses browser to read user credentials to websites.
    - can overwrite MBR.
    - or begin encrypting file in home dir.
- **Shamoon**
    - 2010, MS windows in energy sector. data stealing. variant appeared in 2017 again.

- **Gameover Zeus**, **Mirai**, **Linux Encoder1**, **Kedi RAT** etc..



- **Ransomware**
    - kind of malware. e.g. CryptoLocker - 2013.
    - first - 1989, PC Cyborg Trojan.
    - WannaCry - 2017 - healthcare systems in UK, attacked unpatched Windows systems.
    - Bad Rabbit - 2017 - virus/ransomware. - Russia/Ukraine.

- **Types of Viruses** - by its propagation method or by activities on the target computers.

    - **Macro**: infect the macros in Office Docs. (VBA) or VBScript.
    - **Boot Sector**: infects boot sector of the drive.
    - **Multipartite**: attack in multiple ways.
    - **Memory resident**: installs and then remains in RAM, till computer in online.
    - **Armored**: uses techs that make it hard to analyse. Code confusion, or Compressed code.
    - **Stealth**: attempts to hide itself from antivirus.
    
        - **Sparse infector**: performs malicious activity only sporadically. targets specific program, however it executes every 10th/20th time that progream execures. - reduce freq of attack thus reduce chances of detection.
        - **Encrypted**: encrypted, just enough to prevent antivirus program from recognizing it. decrypted and launched.
        - **Polymorphic**: changes its form from time to time. 
        - **Metamorphic**: can comletely change itself.

### Virus Scanners
- defence against viruses, a software tries to prevent a virus from infecting the system.
- scans incoming emails and other incoming traffic. can scan USBs too.
- work in 2 ways:

    **1**- contains a list of virus files (periodically updated, antivirus scans for known viruses. emails - are checked for subjectline and content. looks for attachments - of certain size, creation date & location. file can be moved to quarantined folder or deleted. - works only for known viruses. 
    
    **2** - by monitoring system for certain behaviours - e.g. programs trying to write to MBR, change system files, alter registry, automate emails or self multiply. - by searching for files that stay in memory after they are executed (TSRs - Terminate and Stay Resident, could be legitimate programs).

- additional methods - scanning system files, monitor programs trying to modify these.
- ondemand virus associationing and ongoing scanners.


- **Email and Attachment Scanning**
    - examine email and email server before downloading.
    - scan email/attachment before it reaching outlook.
    - scan on server before sending to clients.

- **Download Scanning**
    - any ftp/http download should be scanned.

- **File Scanning**
    - for files copied over from network, shared drive or already present in machine before antivirus installed.
    - ondemand or ongoing.
    - can find already known viruses, and may not find any new ones.

- **Heuristic Scanning**
    - most advanced form of virus scanning.
    - uses rules to determine whether a file/program is behaving like a virus.
    - can find new viruses, not fool-proof.
    - may have false positives and negatives.
    - as it is becoming more accurate, more and more will employ this method.

- **Active Code Scanning**
    - most websites have embeded active codes (java applets/ActiveX).

- **Instant Messaging Scanning**
   - relatively new
   - looks for known signatures.

- Most virus scaners use a Multi-Modal approach, i.e. applies one or more of the scanning approaches discussed above.

### Antivirus
Considerations when purchasing -
    - **Budget**
    - **Vulnerability**
    - **Skill**
    - **Technical**

- **McAfee**
- **Norton Antivirus**
- **Avast Antivirus**
- **AVG**
- **Kaspersky**
- **Panda**
- **Malwarebytes**
- **Antivirus Policies and Procedures**
    - always use virus scanner
    - do not open attachment if in doubt/unexpected email.

### Virus Infection and Identification
- What to do, if systems/network infected with virus - focus on:
    - **Stopping the Spread of Virus**
      - first priority - will depend on how much virus has spread.
      - if infection is on a segment of WAN/LAN - disconnect from that WAN/LAN.
      - disconnect servers (with sensitive data) from machines infected.
      - disconnect backup devices.
      - goal is to avoid virus infecting critical resources.
    - **Removing the virus**
      - once isolated, clean the virus - using antivirus/ or virus removal steps.
      - if cannot remove/format machines (check backups before ;))
      - scan machines again.

    - **Finding out how the infection started**
      - once contained and removed, check how it sarted - so it doesnt reappear again.
      - get feedback from users.
      - read about virus.
      - monitor for activity on network.

### Trojan Horses.
- educate users not to download from unknown sited.
- most common actions TH take:
  - Erase files from computer
  - Spread other malwares/viruses (dropper)
  - using host computer to launch DDoS.
  - search for PII, such as bank account details.
  - Install backdoor on system.
  - famous TH - Back Orifice, Anti-Spyware 2011, Shedun, Brain Test, FinFisher, NetBus, FlashBack.

- **Trohan Horses Symptons**
  - difficult to determine.
  - number of symptoms - home page of browser changing, user/pwd/account changed, screensavers, mouse setting, backgrounds changes, Any device working on its own (CD etc).


### Sypware or Adware
- can compromise some sensitive information
- consume too much systems resources
- both use memory.
- difference bw Spyware and adware is, they both infect machine in same manner. Spyware seeks to obtain info from machine. Adware seeks to create Pop-up ads.
- growing problem for nw security and home pc security.
- famous types of Adware and Spyware
  - Gator
  - RedSheriff

-**Anti-Spyware**
- excellent way to defend against spyware and adware.
- essential as running Antivirus
- spyware can be a vehicle or purposeful industrial espionage.
