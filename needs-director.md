# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given - Hospital is working
  And - There are two separate registers for working days and holidays
  When - Patient admits in hospital
  Then - Make entry in the respective register

Scenario: Compute parking slots to reserve for visiting specialists

  Given - Hospital is working and has parking
  When - A vehicle enters
  And - checks if it is a specialist's vehicle or not
  And - if there are more than 3 free slots
  Then - give one slot to the vehicle (!specialists)
  And - give one of the three  reserved spot to specialist
