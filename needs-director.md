# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given A patient has an entry card
  When The patient visits the hospital
  Then Show Patient visit

Scenario: Compute parking slots to reserve for visiting specialists

  Given The visitor is a Specialist
  When The specialist is going to visit
  Then Compute and determine parking slots if available
  
Scenario: Show patient visits-counts per shifts

  Given The sensor is able to make an entry for the visitor in the system
  database and the system knows the schedule of the shifts
  When The director requests for fetching the data
  Then Visitor count increases by 1 and the back end stores the previous
  shift count and counter resets to 0 when the shift changes
