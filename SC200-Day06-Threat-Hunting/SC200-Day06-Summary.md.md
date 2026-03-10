\# SC-200 Day 06 — Threat Hunting in Microsoft Sentinel



\## Business Scenario

BrightSpark Electrical Services Ltd is a small electrical contractor company with around 20 employees. The business wants to improve its security monitoring by proactively searching for suspicious activity instead of relying only on automatic alerts or incidents.



\## Business Problem

Some suspicious behaviour, such as repeated failed sign-ins, unusual account activity, or early attacker reconnaissance, may not immediately trigger a high-confidence alert. This means potential threats could remain unnoticed unless the SOC analyst manually hunts through the available logs.



\## Security Goal

Use Microsoft Sentinel hunting capabilities and KQL queries to proactively detect suspicious authentication and activity patterns, validate whether they are benign or potentially malicious, and strengthen the investigation process.



\## What I Built Today

Today I used Microsoft Sentinel Hunting to proactively search available log data using KQL queries. I reviewed suspicious authentication patterns, investigated failed sign-ins, and documented findings using a structured SOC workflow.



\## Key Concepts

\- Microsoft Sentinel Hunting

\- Threat hunting

\- KQL queries

\- Authentication analysis

\- Failed sign-in review

\- Proactive SOC operations

\- Analyst-driven investigation

\- Log correlation



\## What I Learned

Today I learned how to use Microsoft Sentinel for proactive threat hunting instead of relying only on incidents or analytics rules. I used KQL queries to search through available security data, identify suspicious behaviour patterns, and think through how a SOC analyst would validate findings and decide whether deeper investigation or escalation was needed.

