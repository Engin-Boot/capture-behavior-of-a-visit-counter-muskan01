# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given - Hospital is working
  When - a visitor enters a hospital
  Then - entry card issues for the time he/she is there

Scenario: Alert when seating capacity is full

  Given - Hospital is working
  And - it has n seats
  When - an entry card issues to visitor
  And - if current entry cards issues minus visitors exit
  is equal to n
  Then - Alert the staff about seating capacity
