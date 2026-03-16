## Metric Filter Configuration
Filter name: FailedConsoleLoginFilter
Filter pattern: { ($.eventName = "ConsoleLogin") && ($.errorMessage = "Failed authentication") }

Metric namespace: SecurityMonitoring
Metric name: FailedConsoleLogin
Metric Value: 1

Purpose:
This metric filter detects failed AWS console login attempts from CloudTrail logs.
