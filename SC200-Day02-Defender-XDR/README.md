\# SC-200 Day 02 — Microsoft Defender XDR (Investigation Flow + Advanced Hunting Baseline)



\## Overview

This lab validates Microsoft Defender XDR access and documents the SOC investigation workflow (signals → alerts → incidents → entity pivots → hunting → response).  

In this tenant, alerts/incidents were not available yet, so Day 02 focused on baseline validation using portal checks and Advanced Hunting schema/queries.



\## Objectives

\- Validate access to Microsoft Defender XDR (Incidents, Alerts, Advanced Hunting)

\- Confirm current alert/incident state in the tenant

\- Validate Advanced Hunting schema availability and execute baseline KQL queries

\- Document investigation workflow and next steps to enable telemetry



\## Architecture (Diagram 01)

\- Diagram: `SC200-Day02-Diagram-01-DefenderXDR-Investigation-Flow.png`

\- Flow: Signals/Telemetry → Defender XDR correlation → Alerts → Incidents → Entity pivots → Advanced Hunting (KQL) → Response/Close



\## Tenant State (Evidence-Based)

\- Alerts/Incidents: 0 (in selected time range)

\- Advanced Hunting schema tables available:

&nbsp; - `AlertEvidence`

&nbsp; - `BehaviorEntities`

&nbsp; - `BehaviorInfo`

\- Note: `DeviceInfo` table not available (endpoint telemetry/MDE not onboarded yet)

\- Next step: onboard an endpoint / enable signal sources to generate richer telemetry and incidents



\## KQL Queries (stored in /04-KQL-Queries/)

\- `SC200-Day02-Hunting-Query01.kql`  

&nbsp; - `AlertEvidence | take 50`

\- `SC200-Day02-Hunting-Query02.kql`  

&nbsp; - `BehaviorEntities | take 50`



\## Evidence (Screenshots)

Stored in: `/03-Evidence/`  

Recommended filenames:

\- SC200-Day02-01-DefenderXDR-Portal-Home.png

\- SC200-Day02-02-DefenderXDR-Alerts-0.png

\- SC200-Day02-03-DefenderXDR-Incidents-0.png

\- SC200-Day02-04-AdvancedHunting-Schema-DeviceTables.png

\- SC200-Day02-06-AdvancedHunting-Query01-Results.png

\- SC200-Day02-07-AdvancedHunting-Query02-Results.png



\## What This Lab Proves

\- Defender XDR provides a unified SOC workflow for alert/incident investigation.

\- Advanced Hunting schema availability depends on enabled/onboarded Defender data sources.

\- Baseline validation and evidence-driven documentation are essential before enabling detections at scale.

