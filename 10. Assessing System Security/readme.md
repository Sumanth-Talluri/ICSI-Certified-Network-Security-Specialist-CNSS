## Module 10 - Assessing System Security

### Risk Assessment

- Evaluating security of any network always starts with a risk assessment.
- Involves considering the assets 
- trying to protect, threats against these assets, Vulnerabilities in the systems and measures taken to protect them.
- **Formula** for calculating risk:
   - SLE: Single loss expectancy (impact caused by single loss)
   - AV: Asset value
   - EF: Exposure Factor (%age of valut of asset)

   SLE = AV * EF

- **Next Formula** is:
   - ALE: Annualized loss expectancy (how much loss can be expected from a particular issue in a year)
   - ARO: Annual rate of occurrence

   ALE = SLE * ARO

- **Residual Risk**:
  - how much risk is left over after taking all steps required to deal with it. how to deal with a risk which is identified.

  - **Mitigation**: steps taken to lessen it. no matter what is done, some risk will still be there. It is most common solution.
  - **Avoidance**: difficult to attain. means zero risk. Not usually a viable solution.
  - **Transference**: process of transferring risk to someone else. e.g. cyber breach insurance.
  - **Acceptance**: if probability of risk is very low or cost of mitigation is higher than cost of risk realized, may choose to do nothing. or simply accept the risk.


### Conducting an Initial Assessment

"Six Ps": stages of assessing a system's security.

  - Patch
    - patch regularly
  - Ports
    - block unused ports.
    - also, block unused router ports
  - Protect
    - use IDS/IPS
    - use FWs
    - use Antivirus, antispywares
    - proxy servers
    - use encryption
  - Policies
  - Probe
  - Physical
    - control physical access
       - server room
       - workstations
       - other equipment
    - protect physical copy of data (USB, Tapes, CDs)
    - logs all access

### Probing the NetWork:

- probe the network for Vulnerabilities
- can use various utilities/tools for same
- hackers use similar tools (its like being proactive :))
- Three types of probes (probing tools)
    - Port Scanning - mostly wellknown ports (1-1024)
    - Enumeration - tries to find what is on the network
    - Vulnerability assessment

- tools for Vulnerability scanning:

    - Nessus
    - Qualys
    - Openvas
    - Netsparker
    - Acunetix
    - Nexpose community
    - Retina
    - Core Impact

    ```
    $ nmap ipaddr  ## find open ports
    $ nmap -sV  ipaddr ## find services running on open ports
    ```


### Vulnerabilities
Vulnerability is a flaw in system that an attacker could exploit to attack the system
- **CVE** (Common Vulnerabilities and Exposure) by Mitre - https://cve.mitre.org/ (named as CVE prefix + Year + random digits)
- **NIST** (National Institute of Standards and Technology) - https://nvd.nist.gov/, uses CVE format.
- **OWASP** (Open Web Application Security Project)
  - standard for web app security
  - https://www.owasp.org/
  - provides top10 Vulnerability list.

### Documenting Security
- Physical Security documentation
- Policy and Personnel Documentation
- Probe documents
- Network protection documents
- All above documents should be kept safe (both physical and softcopies)
