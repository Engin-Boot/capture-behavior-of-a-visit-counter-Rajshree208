# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given A patient has an entry card
  When The patient visits the hospital
  Then Show Patient visit

Scenario: Compute parking slots to reserve for visiting specialists

  Given The visitor is a Specialist
  When The specialist is going to visit
  Then Compute and determine parking slots if available
