## Failed Console Login Detection

Log Source: AWS CloudTrail

Filter Pattern:
{ ($.eventName = "ConsoleLogin") && ($.errorMessage = "Failed authentication") }

Alert Trigger:
Metric value >= 1 within 1 minute.

Purpose:
Detect brute-force login attempts or unauthorized access attempts.

Test Scenario:
Multiple incorrect login attempts were performed using the employee-user IAM account.

Result:
CloudWatch alarm triggered, and an SNS email notification was received.
