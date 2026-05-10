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

![Failed Logins](https://github.com/AdityaDNair/soc-log-analysis/blob/main/logs/failed-logins.png?raw=true)

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


