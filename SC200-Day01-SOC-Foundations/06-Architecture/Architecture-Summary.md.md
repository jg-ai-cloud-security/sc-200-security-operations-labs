\# Architecture Summary — SC200 Day 01







SC-200 Day 01 — Diagram 01 Explanation (Sentinel Baseline + Azure Activity Detection)



This architecture shows an end-to-end Microsoft Sentinel SOC workflow using Azure Activity logs as the primary data source (ideal when Entra SigninLogs aren’t available due to licensing).



1\) Event source (Azure Subscription / Tenant scope)



A Security Admin/Operator performs an action in the Azure environment. In this lab, the key event is an RBAC role assignment change (IAM) such as adding or removing a role for a user.



2\) Logging layer (Azure Activity Log)



All control-plane actions in Azure (including RBAC changes) are recorded in the Azure Activity Log. This provides the raw audit trail needed for detection and investigation.



3\) Ingestion into Sentinel (Azure Activity data connector)



The Microsoft Sentinel Azure Activity connector collects Activity Log events from the subscription and forwards them into the SIEM data store.



4\) Centralized storage (Log Analytics Workspace)



Logs are stored in the Log Analytics Workspace (LAW) under the AzureActivity table. This enables KQL queries, detections, workbooks, and long-term analysis.



5\) Detection engineering (Scheduled Analytics Rule)



A Scheduled Analytics Rule runs automatically every 5 minutes with a 1-hour lookback to detect RBAC role assignment changes:



Microsoft.Authorization/roleAssignments/write



Microsoft.Authorization/roleAssignments/delete



When the query matches, Sentinel generates an alert.



MITRE ATT\&CK mapping:



Tactic: Privilege Escalation



Technique: Account Manipulation (T1098)



6\) SOC outcome (Alert → Incident → Triage)



The alert is promoted into an incident, which appears in the Incidents Queue inside the Microsoft Defender (Unified SOC) portal. From there, an analyst can triage, investigate entities (caller, resource group, resource ID), and respond.







\## Overview

This lab establishes a basic Security Operations Center (SOC)

monitoring architecture using Microsoft Sentinel.



\## Components

\- Entra ID: generates authentication logs

\- Log Analytics Workspace: centralized log storage

\- Microsoft Sentinel: SIEM platform

\- Analytics Rules: detect suspicious behaviour



\## Security Flow

User authentication events are collected from Entra ID,

ingested into Log Analytics, analysed by Sentinel,

and converted into incidents for investigation.



\## Security Objective

Enable centralized detection and investigation

capability for identity-based threats.

