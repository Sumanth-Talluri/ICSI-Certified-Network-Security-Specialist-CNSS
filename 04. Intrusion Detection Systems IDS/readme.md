## Module 4 - IDS Concepts
- Six basic approaches.
    - some are used by softwares
    - other are strategies used by orgs.

- **Pre-emptive Blocking** (banishment vigilance)
    - seeks to prevent intrusions before they happen.
    - attempts to detect early footprinting stages of an imminent intrusion. (and block user/ipaddr)
    - e.g. if specific ip is source of frequent port scans etc.
    - quite complicated and could block legitimate user.
    - can lead to false positives.
    - alerts users/admins and then admin can decide.
    - should be used as part of overall IDS strategy.

- **Anomaly Detection**
    - system looks for abnormal behaviour, software compares observed activity against expected normal usage profiles.
    - "trace back" detection.
        - Threshold monitoring (can results in high false positives if used in isolation)
        - Resource profiling (historical usage profiles)
        - User/Group work profiling
        - Executable profiling. (monitors how programs use resources) , enables IDS to identify activity that might indicate an attack.


### Components and Processes of IDS
- basic components and functions of all IDS
    - An activity (data source)
    - The Administrator
    - a sensor (collects data and passes to analyser for analysis)
    - the Analyser (proess that analyses the data)
    - An alert (message from analyser, that an event of interest has occurred)
    - The Manager (part of GUI/console used to manage IDS)
    - the Notification
    - the operator (ofter administrator)
    - An event (and occurrence of suspicious activity)
    - data source

- **Types of IDSs**
    - Active IDS (IPS): will stop any traffic deemed malicious.

    - Passive IDS.: simply logs the activity.

    - HIDS
    - HIPS
    - NIDS
    - NIPS


### Implementing IDS
- **Snort**: open source IDS. software installed on a server, monitors incomfing traffic. works as host-based fw. has 3 modes:
    - **Sniffer**: packets displayed on screen, can check if tramission is encrypted.
    - **Packet Logger**: packet contents is written to a file log.
    - **Network Intrusion-Detection**: uses a heuristic approach to detecting anomalous traffic. requires most configurations.

```
snort -c <configfile> -i1 -l <logfile> -A console
```
- **Cisco Intrusion Detection and Prevention**
    - Cisco IDS 4200 series Sensors
    - Cisco Catalyst 6500 Series IDS Service Module.


### Honeypots
- **Specter** - can simulate major internet protocols/srvices. logs all the activity.
- 5 modes:
    - Open
    - Secure
    - Failing
    - Strange
    - Aggressive
- can configure password file
    - Easy
    - Normal
    - Hard/mean
    - Fun
    - Warning

- **Symantec Decoy Server**
