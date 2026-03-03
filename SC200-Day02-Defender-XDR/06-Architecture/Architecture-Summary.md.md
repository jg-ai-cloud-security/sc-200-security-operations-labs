\# SC-200 Day 02 — Architecture Notes (Defender XDR)



\## Diagram 01 — Defender XDR Investigation Flow

\### What This Diagram Proves — Day 02

\- Defender XDR correlates signals from Endpoint/Email/Identity/Cloud Apps into Alerts and Incidents.

\- SOC investigation pivots through entities (User, Device, IP, Mailbox).

\- Advanced Hunting (KQL) validates and enriches findings before response/closure.



\## Current Tenant State (Evidence-Based)

\- Alerts/Incidents currently 0 in portal.

\- Advanced Hunting schema tables available: AlertEvidence, BehaviorEntities, BehaviorInfo.

\- Next step: onboard endpoint / enable signal sources to generate richer telemetry.

