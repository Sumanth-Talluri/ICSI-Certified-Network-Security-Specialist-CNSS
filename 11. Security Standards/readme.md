## Module 11 - Security Standards

### ISO Standards

- The International Organization for Standardization.
- there are 100s of standards
- Most important for NW Security

    - ISO/IEC 15408: The Common criteria for IT Security Evaluation
    - ISO/IEC 25000: Systems and Software Engineering
    - ISO/IEC 27000: IT - Security Technology
    - ISO/IEC 27001: Information Security Management
    - ISO/IEC 27005: Risk Management
    - ISO/IEC 27006: Accredited Certification Standard
    - ISO/IEC 28000: Specification for security management systems for the supply chain
    - ISO 27002: Information Security Controls
    - ISO 27003: ISMS Implementation
    - ISO 27004: IS Metrics
    - ISO 27005: Risk Management
    - ISO 27006: ISMS Certification
    - ISO 27007: Management System Auditing
    - ISO 27008: Technical Auditing
    - ISO 27010: Inter-organisation communication
    - ISO 27011: Telecommunications
    - ISO 27033: Network security
    - ISO 27034: Application security
    - ISO 27035: Incident Management
    - ISO 27036: Supply chain
    - ISO 27037: Digital forensics
    - ISO 27038: Document reduction
    - ISO 27039: Intrusion prevention
    - ISO 27040: Storage security
    - ISO 27041: Investigation assurance
    - ISO 27042: Analysing digital evidence
    - ISO 27043: Incident Investigation


### NIST Standards
**NIST SP 800-14** - Generally Accepted Principles and Practices for Security IT Systems
- describes common security Principles that should be addressed within security policies
- describe 8 Principles and 14 practices used to develop sec policies
- 8 Principles:
    - Computer security supports the mission of org.
    - Computer security is an integral element of sound management
    - Computer  security should be cost-effective
    - System owners have security responsibilities outside their own Organization.
    - Computer security responsibilities and accountabilities should be made explicit.
    - requires a comprehensive and integrated approach.
    - should be periodically reassessed
    - is constrained by societal factors.


**NIST SP 800-35 - guide to IT security services.**
- six phases of IT security life cycle are defined
    - **Phase 1: Initiation.** org is looking to implement a IT security service, device or process.
    - **Phase 2: Assessment.** involves determining and describing the org's current security posture.  should use quantifiable metrices.
    - **Phase 3: Solution.** This is where various solutions are evaluated and one or more are selected.
    - **Phase 4: Implementation.** IT security service, device or process is implemented.
    - **Phase 5: Operations.** is the ongoing operation and maintenance of sec services, device, or process implemented in P4.
    - **Phase 6: Closeout.** when a system is replaced by newer/better system.


**NIST SP 800-30 Rev.1 - Guide for Conducting Risk Assessments**
- is a standard for conducting Risk Assessments.
- provides guidance on how to conduct it.
- 9 steps
    - **Step 1.** System Characterization
    - **Step 2.** Threat Identification
    - **Step 3.** Vulnerability Identification
    - **Step 4.** Control Analysis
    - **Step 5.** Likelihood Determination
    - **Step 6.** Impact Analysis
    - **Step 7.** Risk Determination
    - **Step 8.** Control Recommendations
    - **Step 9.** Results documentation.

### GDPR (General Data Protection Regulation)
- EU LAW created in 2016
- deals with data privacy
- applied to any entity (Business, govt, agency etc), that either collects data or processes it.
- Even if org is not within EU, if it has EU data, GDPR applied.


### PCI DSS - Payment Card Industry Data Security Standard.

- is a proprietary Information security standard for orgs that handle cardholder info for major credit/debit cards such as VISA and MasterCard
- several goals
- **Requirements** :

    **1.1** FW and router system should be installed to protect cardholder info.
    
        - Program the standards of firewall and router to:
            1. Perform testing when configs change.
            2. Identify all connections to cardholder info
            3. Review config rules every 6 months.
        - Configure firewall to prohibit unauthorised access from networks and hosts and deny direct public access any info about the cardholder.
        - Additionally, install firewall software on all computers that access the orgs PCI compliance network.

    **1.2** Change all default pwds.

    **2.1** Cardholder data (any personal info about the cardholder that is found on the payment card) can never be saved by a merchant.
    
        - includes  preserving encrypted authentication data after authorization.
        - Merchants can only display the max of the first 6 and last 4 digits of PAN (primary account number).
        - If merchant stores PAN, ensure that data is secured by saving it in a cryptographic form.

    **2.2** all info is encrypted when transmitting the data across public nw.

    **3.1** Computer viruses can spread in many ways, but mainly through emails and other online activities. Merchants computer should have latest antivirus software defs (and on all computers in nw)

    **3.2** must install vendor-provided security patches within a month of the release. security alert programs, scanning services or software may be used to signal the merchant of any vulnerable info.

    **4.1**
    
        - must limit accessibility of cardholder info.
        - Install pwds and other security measurements to limit employees access to cardholder data.
        - Only employees who must access the info to complete their job, should be allowed.

    **4.2** assign each user an unreadable pwd used to access the cardholder data.

    **4.3**
    
        - Monitor the physical access to cardholder data.
        - do not allow unauthorized persons the opportunity to retrieve the info by getting physical/digital.
        - destroy all outdated info.
        - maintain a visitor log and save for atleast 3 months.

    **5.1**
    
        - keep system activity logs that trace all activity and review daily.
        - info in logs is useful in event of a security breach
        - to trace employee activities and locate the source of violation.
        - Record entries should have at least - user, event, date n time, success or failure, source of affected data  and system components.

    **5.2**
    
        - Each quarter, use a wireless analyser to check for wireless access points to prevent unauthoriized access.
        - scan internal/external nw to identify any possible vulnerable areas in the system.
        - install sw to recognise any modification by unauthorised personnel.
        - ensure that all IDS/IPS engines are up to date.
