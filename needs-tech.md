# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given A server is available and is accessible
  and we have a cache memory to copy the visit-counts
  When The server restarts
  Then Recover the visit-counters from the cache

Scenario: Reconcile counts if the sensor is offline for a while

  Given A sensor senses the count of visitors and sends the data to the server
  When The sensor is offline
  Then Reconcile counts data from the server
