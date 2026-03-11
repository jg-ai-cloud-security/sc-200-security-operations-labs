\# SC-200 Day 07 Architecture



\## Architecture Summary

This diagram shows how security telemetry flows into Microsoft Sentinel and supports the incident investigation process from data ingestion through triage and response.



\## Components

\- Data Sources (Entra ID, Defender, Alerts)

\- Microsoft Sentinel (Analytics + Incident Creation)

\- Incident Queue

\- Incident Details (Alerts, Entities, Investigation Graph)

\- KQL Validation in Log Analytics

\- SOC Analyst Triage

\- Response Actions / Incident Closure



\## What This Diagram Proves

\- Sentinel can centralize security signals from multiple Microsoft sources

\- Incidents provide a structured investigation workflow

\- Analysts can review incident context and supporting evidence

\- KQL can be used to validate suspicious activity

\- SOC analysts can document response actions and closure decisions



\## Lab Note

For Day 07, a manual test incident was created to simulate the investigation workflow. Because the incident was manually created, linked alerts, entities, and investigation graph data may be limited.

