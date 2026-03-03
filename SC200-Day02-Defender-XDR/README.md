\# SC-200 Day 01 — Sentinel Baseline + Azure Activity Detection



\## Overview

This lab establishes a Microsoft Sentinel baseline using the Unified Security Operations experience (Microsoft Defender portal) and validates an end-to-end SOC workflow using Azure Activity logs.



A scheduled analytics rule detects Azure RBAC role assignment changes and generates an alert → incident for investigation.



\## Objectives

\- Deploy and enable Microsoft Sentinel on a Log Analytics Workspace

\- Connect Azure Activity logs to Sentinel

\- Validate ingestion using KQL queries

\- Create a scheduled analytics rule to detect RBAC changes

\- Generate test RBAC events and confirm incident creation

\- Document evidence and architecture



\## Architecture (Diagram 01)

\- Diagram: `SC200-Day01-Diagram-01-Sentinel-Baseline-AzureActivity.png`

\- Flow: Admin action → Azure Activity Log → Sentinel connector → Log Analytics (AzureActivity) → Analytics rule → Alert/Incident → Defender Incidents Queue



\## Resources Created

\- Resource Group: `rg-sc200-sentinel-day01-uks-001` (update if different)

\- Log Analytics Workspace: `law-sc200-day01-uks-001` (update if different)

\- Microsoft Sentinel enabled on workspace



\## Data Sources / Connectors

\- ✅ Azure Activity (connected to subscription and sending events to LAW)



\## Detection Rule Created

\*\*Name:\*\* `SC200-D01 - Azure RBAC Changes Detected`  

\*\*Type:\*\* Scheduled analytics rule  

\*\*Schedule:\*\* Run every 5 minutes  

\*\*Lookback:\*\* 1 hour  

\*\*Creates incident:\*\* Yes  

\*\*MITRE ATT\&CK:\*\* Privilege Escalation → Account Manipulation (T1098)



\## KQL (stored in /04-KQL-Queries/)

```kql

AzureActivity

| where TimeGenerated > ago(1h)

| where OperationNameValue has\_any (

&nbsp; "Microsoft.Authorization/roleAssignments/write",

&nbsp; "Microsoft.Authorization/roleAssignments/delete"

)

| project TimeGenerated, Caller, OperationNameValue, ActivityStatusValue, ResourceGroup, ResourceId

| order by TimeGenerated desc

