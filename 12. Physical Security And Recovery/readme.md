## Module 12 - Physical Security and Recovery

### Physical Security
- main target is to physically secure machines.
- securing issues, such as controlling access to building and knowing how to respond to fires etc.
- Monitoring systems such as alarms and cameras are also part of physical security.

**Equipment Security**
- control access to the building, to key rooms within building.
- locked door on server room.
- should also have a way to control who can access that room
- swipe card, password key entry or biometric system, track who entered and when
- room should not have windows (or reinforced windows), outsiders should not be able to view inside.
- room should be fireproof.
- routers, switches - if distributed, should be secured too.
- can use locked closets.
- workstations can be locked to respective desks.
- any device, which is valuable or contains valuable data must be physically secured.
- Ability to remotely wipe mobile devices.


**Securing Building Access**
- fences
- parking lots
- entry to building.
- Lighting


**Monitoring**
- CCTV/Video monitoring
- place in or around the building
- should have unobstructed view on the area to be monitored
- all entrances and exits should be monitored.
- outside critical areas.
- cannot be easily disabled.
- can transmit recordings to remote location.
- signal/feed is secure.


**Fire Protection**
- adequate fire alarms and fire extinguishers.
- Fire extinguishers
   - class A: Ordinary combustibles such as wood or paper.
   - Class B: Flammable liquids such as grease, oil or gasoline
   - Class C: Electrical equipments
   - Class D: Flammable metals
 - Fire suppression systems should be used.



### Disaster Recovery
- Any event that can significantly disrupt orgs operations
- Disaster Recovery Plan (DRP) - guide to return business to normal operations.
    - contact personal details
    - specific tasks assigned to specific people
    - clear responsibility
        - Locating alternative facilities
        - Getting equipment to those facilities
        - Installing and configuring sw
        - setting up the nw at new facility
        - Contacing staff, vendors and customers

**Business Continuity Plan (BCP)**
- same as DR but different focus.
- DRP is designed to get org back to full functionality as quickly as possible.
- a BCP is designed to get minimal business functions back up and running up to a certain level in order to conduct some type of business.


**Determining Impact on Business**
- before BCP or DRP, a BIA (business impact analysis, of what damage to org a given disaster might cause) is required
- consider MTD (Maximum Tolerable Downtime) - how long can system be down.
- MTTR (Mean time to Repair/Recover)
- MTBF (mean time between Failures)


- RTO (Recovery Time Objective) - is the time by which service is intended to be back online, if there is a failure.
- It should be less than MTD

- RPO (Recover Point Objective) - how much data loss is Tolerable.


**Testing DR**
- once both DRP and BCP in place, should be periodically tested, ensure these work as expected. Type of tests - in order from least intrusive, easiest -> most difficult and most informative.
    - Document Review/Checklist. - usually done by individual
    - Walkthrough/Tabletop. - is a team effort.
    - Simulation
      - simulates some sort of Disaster
      - team or individual.
      - get "what if" scenarios
      - check if everyone knows their part in case of disaster.
    - Parallel
      - test if all backup systems came online.
      - includes restoring backup, turning on backup systems.
      - initializing secondary communication systems.
    - Cut-off/Full Interruption
      - shutdown production system and see if BCP/DRP works.
      - good way to check plans
      - can cause disaster if doesnt work.
      - should be done only if all of above tests are complete.
      - in fact all these should be done in order.
      - should schedule this during downtime.


### Fault Tolerance

- equipments fail
- so plan for tolerant to these
- backup
- different backups
   - Full
   - Differential
   - Incremental

- RAID
  - RAID 0
  - RAID 1
  - RAID 3 or 4
  - RAID 5
  - RAID 6
  - RAID 1 + 0
  
