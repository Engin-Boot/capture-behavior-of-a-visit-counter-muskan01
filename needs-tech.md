# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given - Hospital is working
  And - Server restores the information
  When - Server fails
  And - Server restores
  Then - Lost information recovers
  And - it starts counting again

Scenario: Reconcile counts if the sensor is offline for a while

  Given - Hospital is working
  And - Sensor at the entrance counts visitor
  When - Sensor goes offline for a while
  And - if there is a visitor, the entry goes in a register
  Then - restart the counting with updated numbers
