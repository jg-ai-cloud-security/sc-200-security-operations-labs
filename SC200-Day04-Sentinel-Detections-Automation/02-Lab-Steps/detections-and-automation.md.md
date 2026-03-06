# Lab Steps – Brute Force Detection Rule

## Objective
Create a Microsoft Sentinel analytics rule to detect multiple failed login attempts using Windows Security Event logs.

## Steps

1. Navigate to Microsoft Sentinel.
2. Open the Analytics section.
3. Create a new Scheduled Analytics Rule.
4. Configure rule details.

Rule Name:
SC200-BruteForce-Login-Detection

Severity:
Medium

5. Add the detection query.

## Detection Query

SecurityEvent
| where EventID == 4625
| summarize FailedAttempts=count() by Account, IpAddress, Computer
| where FailedAttempts >= 5

6. Configure rule scheduling.

Run query every: 5 minutes  
Lookup data from last: 5 minutes

7. Enable incident creation.

8. Save and deploy the rule.

## Result

The rule will trigger an incident when multiple failed login attempts are detected.