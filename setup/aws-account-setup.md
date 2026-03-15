# AWS Account Security Setup
Before building the cloud security monitoring lab, the AWS root account was secured to follow security best practices.

## Security Controls Implemented
1. Enabled Multi-Factor Authentication (MFA) for the root account
2. Configured AWS billing alerts to prevent unexpected charges
3. Verified access to the AWS Management Console

## Why This Step Is Important
Root account compromise can lead to complete control of the AWS environment

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

