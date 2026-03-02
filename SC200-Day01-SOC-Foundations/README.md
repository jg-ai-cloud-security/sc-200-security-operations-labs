SC-200 Day 01 — Sentinel Baseline + Azure Activity Detection
Overview

This lab establishes a Microsoft Sentinel baseline using the Unified Security Operations experience (Microsoft Defender portal) and validates an end-to-end SOC workflow using Azure Activity logs.
A scheduled analytics rule detects Azure RBAC role assignment changes and generates an alert → incident for investigation.

Objectives

Deploy and enable Microsoft Sentinel on a Log Analytics Workspace

Connect Azure Activity logs to Sentinel

Validate ingestion using KQL queries

Create a Scheduled Analytics Rule to detect RBAC changes

Generate test RBAC events and confirm incident creation

Document evidence and architecture

Architecture (Diagram 01)

Diagram: SC200-Day01-Diagram01-Sentinel-Baseline-AzureActivity.png
Flow: Admin action → Azure Activity Log → Sentinel connector → Log Analytics (AzureActivity) → Analytics rule → Alert/Incident → Defender Incidents Queue

Resources Created

Resource Group: rg-sc200-sentinel-day01-uks-001 (update if different)

Log Analytics Workspace: law-sc200-day01-uks-001 (update if different)

Microsoft Sentinel enabled on workspace

Data Sources / Connectors

✅ Azure Activity (connected to subscription and sending events to LAW)

Detection Rule Created
1) Azure RBAC Changes Detected

Name: SC200-D01 - Azure RBAC Changes Detected

Type: Scheduled analytics rule

Schedule: Run every 5 minutes

Lookback: 1 hour

Creates incident: Yes

MITRE ATT&CK: Privilege Escalation → Account Manipulation (T1098)

KQL (stored in /04-KQL/):

AzureActivity
| where TimeGenerated > ago(1h)
| where OperationNameValue has_any (
  "Microsoft.Authorization/roleAssignments/write",
  "Microsoft.Authorization/roleAssignments/delete"
)
| project TimeGenerated, Caller, OperationNameValue, ActivityStatusValue, ResourceGroup, ResourceId
| order by TimeGenerated desc
Test Performed (to Trigger Alert/Incident)

Added and removed an Azure role assignment (Reader) in Subscription → Access control (IAM)

Confirmed the RBAC change appeared in AzureActivity

Confirmed Alert/Incident appeared in Microsoft Defender → Incidents

Evidence (Screenshots)

Stored in: /03-Evidence-Screenshots/

Recommended filenames:

SC200-Day01-01-RG-Created.png

SC200-Day01-02-LAW-Created.png

SC200-Day01-03-Sentinel-Enabled.png

SC200-Day01-04-DataConnector-AzureActivity-Connected.png

SC200-Day01-05-KQL-AzureActivity-Visible.png

SC200-Day01-06-AnalyticsRule-AzureRBAC-General.png

SC200-Day01-07-AnalyticsRule-AzureRBAC-Logic.png

SC200-Day01-08-AnalyticsRule-AzureRBAC-IncidentSettings.png

SC200-Day01-09-Incident-Created.png

Notes / Limitations

Entra SigninLogs ingestion may be unavailable due to tenant licensing requirements (P1/P2).

Day 01 detection pipeline was validated using AzureActivity, which works in standard Azure subscriptions.

What This Lab Proves

Azure control-plane actions are ingested into Sentinel via Azure Activity

Logs are centralized in Log Analytics (AzureActivity table)

Scheduled analytics rules running every 5 minutes can generate alerts and incidents

Incidents are triaged in the Microsoft Defender (Unified SOC) portal