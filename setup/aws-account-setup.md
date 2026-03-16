# AWS Account Security Setup
Before building the cloud security monitoring lab, the AWS root account was secured to follow security best practices.

## Security Controls Implemented
1. Enabled Multi-Factor Authentication (MFA) for the root account
2. Configured AWS billing alerts to prevent unexpected charges
3. Verified access to the AWS Management Console

## Why This Step Is Important
Root account compromise can lead to complete control of the AWS environment.

## Tools Used
- AWS IAM
- AWS Billing Alerts

## Verification
The following security measures were verified:
- MFA successfully enabled for the AWS root account
- Billing alert configured for $5 monthly spend
- AWS console access tested

Screenshots of these configurations will be added to the '/screenshots'  directory.

## CloudTrail Logging Setup
AWS CloudTrail was enabled to record all API activity within the AWS environment.

Configuration:
Trail name: security-monitoring-trail
Log storage: Amazon S3
Management events: Read and write events enabled
Log file validation: Enabled

Purpose:
CloudTrail provides a complete audit trail of actions performed in the AWS account. These logs will later be used for security monitoring and threat detection.

Log file validation: Enabled to ensure log integrity and prevent tampering.

## CloudTrail Integration with CloudWatch
CloudTrail logs were integrated with Amazon CloudWatch Logs to enable real-time monitoring and the creation of alerts.

Configuration:
Trail name: security-monitoring-trail
CloudWatch log group: cloudtrail-security-logs
IAM role: CloudTrail_CloudWatchLogs_Role

Purpose:
Sending logs to CloudWatch enables the creation of detection rules and automated alerts for suspicious activity.

## CloudWatch Log Verification
The CloudTrail logs were successfully delivered to CloudWatch Logs.

Log group:
cloudtrail-security-logs

Sample observed fields:
- eventName
- eventSource
- awsRegion
- sourceIPAddress
- userIdentity

Example observed event:
- ListWirelessGatewayTaskDefinitions

This confirms that AWS activity is being recorded and is available for monitoring and alert creation.


