# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given - There is a entry card allotment system with report generation system
  When - a visitor enters a hospital
  And - entry card issues to the visitor
  And - Entry card allotment system updates
  Then - Report generates according to the entry card allotment system

Scenario: Alert when seating capacity is full

  Given - Hospital is working
  And - it has n seats
  When - an entry card issues to visitor
  And - if current entry cards issues minus visitors exit
  is equal to n
  Then - Alert the staff about seating capacity
