# SC-200 Day 04 — Sentinel Detections + SOAR (Automation)

## Overview
Today I focused on detection engineering in Microsoft Sentinel by turning KQL queries into scheduled analytics rules and proving SOAR automation using an Automation Rule + Playbook (Logic App).

## Objectives
- Create and test 3 KQL detections
- Convert each detection into a Scheduled Analytics Rule (SOC cadence: every 5 minutes)
- Generate Sentinel incidents and validate entity mapping (Account / Host / IP)
- Build an Automation Rule to trigger a Playbook when incidents are created
- Save a workbook to visualise incidents/detections

## What I Built
### Detections (KQL)
- Brute-force style failed logons (threshold-based)
- New admin/group membership change detection
- Suspicious PowerShell execution patterns

Saved in: `/04-KQL-Queries`

### Analytics Rules
- 3 Scheduled query rules created
- Frequency: 5 minutes
- Lookback: 10 minutes
- Entity mapping enabled
- Incident creation enabled
- Grouping/tuning applied to reduce noise

### SOAR Automation
- Playbook (Logic App) triggered on incident creation
- Automation Rule configured to auto-run playbook
- Proof action: playbook adds a comment to the incident (run history captured)

### Visibility
- Workbook saved to monitor incidents/detections

## Evidence (Screenshots)
Stored in: `/03-Evidence`
- SC200-Day04-01-Workspace-DataConnected.png
- SC200-Day04-02-KQL-*-Query-Test.png
- SC200-Day04-03-AnalyticsRule-*-Created.png
- SC200-Day04-04-EntityMapping-Configured.png
- SC200-Day04-05-Incident-Created.png
- SC200-Day04-06-AutomationRule-Created.png
- SC200-Day04-07-Playbook-Run-History.png
- SC200-Day04-08-Incident-Comment-AddedByPlaybook.png
- SC200-Day04-09-Workbook-Saved.png

## Challenges / Notes
- Licensing constraints (no P1/P2). Focus remained on Sentinel-native detections + automation proof using available data sources.

## Key Takeaways
- Running analytics rules every 5 minutes is realistic for SOC operations and improves time-to-detect.
- Entity mapping is critical because it makes incidents investigation-ready.
- Automation Rules + Playbooks provide repeatable response actions and consistent SOC workflow.

## Next Steps (Day 05)
- Add Watchlists (VIP users, risky IPs) for enrichment
- Improve workbook visuals and add custom tiles
- Expand detections with better thresholds, suppression and grouping