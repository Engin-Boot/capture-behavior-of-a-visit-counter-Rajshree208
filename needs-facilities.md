# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given We have the record for the visitor count for each day
  When we have two or more days data
  Then Generate a trend report

Scenario: Alert when seating capacity is full

  Given We have the counter for patient visits
  When The (number of available seats-counter) equal to zero
  Then Alert that the seating capacity is full
