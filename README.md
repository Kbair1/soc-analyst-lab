# SOC Analyst Lab – Brute Force Detection

## Overview

This project demonstrates detection of brute force login attempts using Splunk SIEM.

## Tools Used

* Splunk Enterprise
* Log analysis

## Detection Query

```spl
"Failed password" | rex "from (?<ip>\d+\.\d+\.\d+\.\d+)" | stats count by ip
```

## Findings

* 192.168.1.10 → 6 attempts (attacker)
* 10.0.0.5 → 1 attempt

## Screenshot

![Detection](screenshots/splunk-bruteforce-detection.png)

## Skills Demonstrated

* SIEM log analysis
* Threat detection
* Regex extraction
* Event correlation
