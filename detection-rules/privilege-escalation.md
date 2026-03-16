# Privilege Escalation Detection

Log Source: AWS CloudTrail

Filter Pattern:
{ ($.eventName = AttachUserPolicy) || ($.eventName = AddUserToGroup) || ($.eventName = PutUserPolicy) || ($.eventName = CreatePolicy) }

Purpose:
Detect attempts to grant elevated permissions to AWS users.

Test Scenario:
AdministratorAccess policy was attached to the employee-user.

Result:
CloudWatch alarm triggered and SNS notification was generated.
