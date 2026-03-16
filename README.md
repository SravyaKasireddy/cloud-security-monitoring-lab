# Cloud Security Monitoring Lab (Amazon Web Services)
This project demonstrates a cloud security monitoring environment built in AWS.
The system collects cloud activity logs, detects suspicious behavior, and generates automated security alerts.

The goal of this lab is to simulate a cloud Security Operations Center (SOC) that monitors threats in AWS environments.

## Security Architecture

User Activity
AWS CloudTrail (API Logging)
CloudWatch Logs
CloudWatch Metric Filters
CloudWatch Alarms
SNS Email Notifications
GuardDuty Threat Detection

## AWS Services Used

- AWS IAM
- AWS CloudTrail
- Amazon CloudWatch
- Amazon SNS
- Amazon GuardDuty
- Amazon S3

## Security Detections Implemented
### 1. Failed Login Detection
Detects failed AWS console authentication attempts.

### 2. Privilege Escalation Detection
Detects suspicious permission changes, such as attaching policies or adding users to privileged groups.

### 3. S3 Permission Change Detection
Detects S3 bucket permission changes that could expose data publicly.

---

## Alerting System
Security alerts are automatically sent via:
Amazon SNS Email Notifications

---

## Attack Simulations Performed
The monitoring system was validated by simulating the following scenarios:

- Multiple failed AWS login attempts
- Privilege escalation attempts using IAM policy attachment
- S3 permission modification event

Each scenario triggered CloudWatch alarms and generated SNS alerts.

---

## Key Security Concepts Demonstrated
- Cloud activity logging
- Threat detection using log analysis
- Automated alerting
- Cloud security monitoring architecture
- AWS security best practices

---

## Future Improvements
- Integration with SIEM platforms
- Automated incident response using AWS Lambda
- MITRE ATT&CK mapping for detections
- Security dashboards visualization

---

## Author

Personal Cloud Security Project
