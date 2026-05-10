# soc-log-analysis
SOC-focused log analysis project for detecting failed logins, suspicious authentication activity, and brute-force attack patterns using Linux authentication logs.

## Failed Login Analysis
Authentication logs were analyzed to identify failed login attempts and suspicious authentication activity.
Multiple failed password attempts were detected from external IP addresses targeting privileged accounts such as `root` and invalid users including `admin` and `test`.
Repeated failures occurring within short time intervals may indicate:
- Brute-force attack attempts
- Unauthorized access attempts
- Credential guessing activity
The IP address `203.0.113.45` demonstrated repeated failed login attempts targeting the root account, making it highly suspicious.


![Failed Logins]()

## Suspicious IP Analysis
Authentication logs were reviewed to identify IP addresses associated with suspicious activity.
Several failed login attempts originated from the following IP addresses:
- `203.0.113.45`
- `192.168.1.50`
- `198.51.100.25`
The IP address `203.0.113.45` was identified as the most suspicious due to repeated failed login attempts targeting the `root` account within a short time period.
Indicators suggesting suspicious behavior included:
- Repeated authentication failures
- Attempts targeting privileged accounts
- Rapid login attempts from the same source IP
This type of activity is commonly associated with brute-force attacks and unauthorized access attempts.

![Suspicious IP Analysis](https://github.com/AdityaDNair/soc-log-analysis/blob/main/logs/suspicious-ip-analysis.png?raw=true)


## Suspicious IP & Brute Force Analysis
Authentication logs were analyzed to identify suspicious IP addresses and repeated authentication failures associated with potential brute-force activity.
The following IP addresses demonstrated suspicious behavior:
- `192.168.1.50`
- `203.0.113.45`
- `198.51.100.25`
### Analysis of Suspicious Activity
The IP address `192.168.1.50` repeatedly attempted to authenticate using the invalid username `admin`. Multiple failed attempts within a short time period may indicate username enumeration or credential guessing activity.
The IP address `203.0.113.45` demonstrated repeated failed login attempts targeting the privileged `root` account at the following timestamps:
- 10:20:12
- 10:20:15
- 10:20:18
This repetitive authentication behavior strongly suggests a potential brute-force attack or automated password guessing attempt.

### Indicators Observed
- Repeated failed login attempts
- Rapid authentication attempts within seconds
- Multiple attempts from the same source IP
- Targeting of privileged accounts (`root`)
- Attempts against invalid usernames (`admin`, `test`)
Such patterns are commonly associated with:
- Brute-force attacks
- Credential guessing
- Unauthorized access attempts
- Reconnaissance activity

![Suspicious IP and Brute Force Analysis](https://github.com/AdityaDNair/soc-log-analysis/blob/main/logs/brute-force-pattern.png?raw=true)


## Log Filtering & Investigation Techniques
Log filtering techniques were applied to isolate suspicious authentication events and improve investigation efficiency.
The logs were filtered based on:
- Failed password attempts
- Source IP addresses
- Privileged account targeting (`root`)
- Authentication-related events
  
Filtering suspicious entries helped identify:
- Repeated failed login attempts
- Brute-force behavior
- Suspicious source IP activity
- Privileged account targeting patterns

This process demonstrates basic SOC investigation and event correlation techniques commonly used in security monitoring environments.

![Log Filtering](https://github.com/AdityaDNair/soc-log-analysis/blob/main/logs/log-filtering.png?raw=true)


## Key Learnings

- Understood the structure of Linux authentication logs
- Identified failed login attempts and suspicious authentication activity
- Detected brute-force behavior through repeated failed logins
- Investigated suspicious IP addresses targeting privileged accounts
- Applied basic log filtering and investigation techniques
- Explored SOC-style event monitoring and analysis concepts


## Conclusion

This project provided practical exposure to SOC-focused log analysis and authentication monitoring using Linux authentication logs.

The analysis involved identifying failed login attempts, investigating suspicious IP addresses, detecting brute-force patterns, and applying basic log filtering techniques. Multiple indicators of suspicious authentication behavior were observed, including repeated failed logins targeting privileged accounts such as `root`.

Through this project, foundational cybersecurity concepts related to security monitoring, incident investigation, and threat detection were explored in a hands-on manner. The skills developed are directly relevant to SOC analyst and cybersecurity monitoring roles.


## Repository Structure

soc-log-analysis/
│
├── README.md
│
├── logs/
│   └── auth.log
│
├── screenshots/
│   ├── failed-logins.png
│   ├── suspicious-ip-analysis.png
│   ├── brute-force-pattern.png
│   └── log-filtering.png
│
└── report/
    └── soc_log_analysis_report.pdf

