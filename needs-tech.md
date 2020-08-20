# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given - visitor counting Server is synchronised with cloud
  When - visitor counting system fails
  And - Visitor count is manual until the system recover
  Then - Lost information recovers from cloud and update with manual count

Scenario: Reconcile counts if the sensor is offline for a while

  Given -  visitor counting Server is synchronised with cloud
  When - Sensor goes offline for a while
  And - if there is a visitor, the entry goes in a register
  Then - restart the counting with updated numbers from register
