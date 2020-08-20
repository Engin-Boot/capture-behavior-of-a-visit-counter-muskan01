# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given - There is a system for ID allotment and report generation
  When - Patient visits the hospital
  And - ID issues to the patient
  And - ID allotment system updates
  Then - report is generates according to the ID allotment system

Scenario: Compute parking slots to reserve for visiting specialists

  Given - Specialist's visit schedule
  And - there are sensors which tells the no. of empty slots
  And - there are three spots reserved for specialist's vehicle
  When - A vehicle enters
  And - it is a specialist's vehicle
  Then - give one of the three reserved spot to specialist
