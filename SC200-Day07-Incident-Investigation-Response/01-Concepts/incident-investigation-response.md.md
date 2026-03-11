\# SC-200 Day 07 — Incident Investigation and Response



\## Overview



Security incidents represent confirmed or suspected security events that require investigation and response by a Security Operations Center (SOC).



Microsoft Sentinel enables SOC analysts to investigate incidents by correlating alerts, entities, and log data.



---



\## Key Concepts



\### Security Alert

A security alert is generated when detection logic identifies suspicious activity.



\### Security Incident

An incident groups one or more alerts together to provide context for investigation.



\### Entity Mapping

Entities represent key elements involved in a security event such as:



\- User accounts

\- Host systems

\- IP addresses



Entity mapping helps analysts quickly identify affected assets.



\### Investigation Graph

The investigation graph visualizes relationships between entities and alerts to support faster analysis.



---



\## SOC Investigation Workflow



Alert Generated  

↓  

Incident Created  

↓  

Review Alerts  

↓  

Analyze Entities  

↓  

Investigate Timeline  

↓  

Validate with KQL Queries  

↓  

Determine Response

