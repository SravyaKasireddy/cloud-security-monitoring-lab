## Failed AWS Console Login Detection
This detection rule identifies failed login attempts to the AWS Management Console.

## Log Source
AWS CloudTrail

## Detection Method
ClodWatch metric filter

## Filter Pattern
{ ($.eventName = "ConsoleLogin") && ($.errorMessage = "Failed authentication") }

## Alert Trigger
Metric value >= 1 within 1 minute.

## Notification
Amazon SNS email notification.

## Test Scenario
Multiple incorrect password attempts were made using the IAM user 'employee-user'.

## Result
The CloudWatch alarm 'Failed-AWS-Console-Login' triggered successfully and an SNS email alert was received.

## Security Impact
This rule helps detect potential brute-force login attempts or unauthorized access attempts to AWS accounts.

Metric namespace: SecurityMonitoring
Metric name: FailedConsoleLogin
Metric Value: 1

Purpose:
This metric filter detects failed AWS console login attempts from CloudTrail logs.
