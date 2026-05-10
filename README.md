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
