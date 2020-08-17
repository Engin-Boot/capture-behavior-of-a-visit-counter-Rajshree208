# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given We have the record for the visitor count for each day
  When we have two or more weeks data
  Then Generate a trend report

Scenario: Alert when seating capacity is full

  Given A counter is there for counting the number of seats
  When The (number of available seats-counter) equal to zero
  Then Alert that the seating capacity is full
