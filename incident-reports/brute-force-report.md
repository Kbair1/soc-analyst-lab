## Incident Report: Brute Force Attack Detection

### Summary

Detected repeated failed login attempts indicating a brute force attack.

### Data Source

* auth.log ingested into Splunk

### Investigation Steps

* Queried for failed login attempts
* Extracted IP addresses using regex
* Aggregated attempts by IP

### Findings

* 192.168.1.10 → 6 failed attempts
* 10.0.0.5 → 1 attempt

### Severity

Medium–High

### Mitigation

* Block IP address
* Enable account lockout policy

### Conclusion

Confirmed brute force attack based on repeated failed login attempts.
