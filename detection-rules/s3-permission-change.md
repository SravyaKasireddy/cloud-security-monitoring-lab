# S3 Permission Change Detection

Log Source: AWS CloudTrail

Filter Pattern:
{ ($.eventName = PutBucketAcl) || ($.eventName = PutBucketPolicy) }

Purpose:
Detect potentially dangerous changes to S3 bucket permissions.

Security Risk:
Improper S3 permissions can expose sensitive data publicly.

Result:
CloudWatch alarm triggered when bucket permission changes occurred.
