\# SC-200 Day 06 — Architecture Notes



\## Architecture Overview

This architecture shows how Microsoft Sentinel supports proactive threat hunting across ingested security data.



\## Data Sources

\- Sign-in logs

\- Windows security events

\- Azure activity logs

\- Other connected security sources if available



\## Sentinel Hunting Layer

The hunting layer in Microsoft Sentinel allows analysts to run KQL queries against collected log data to identify suspicious patterns.



\## Analyst Investigation Flow

The analyst reviews query results, validates whether activity looks normal or suspicious, and decides whether to escalate, monitor, or close the finding.



\## Security Value

This approach improves security visibility by identifying weak signals that may not yet have triggered an automated incident.



\## Outcome

Threat hunting supports proactive SOC operations and helps analysts detect suspicious patterns earlier.

