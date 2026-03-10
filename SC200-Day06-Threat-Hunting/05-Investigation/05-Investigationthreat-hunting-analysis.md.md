\# SC-200 Day 06 — Hunting Findings



\## Query 1 Findings

I reviewed failed sign-ins by user to identify accounts with repeated authentication failures. This helps highlight accounts that may be experiencing password spray, brute-force attempts, or normal user error.



\## Query 2 Findings

I reviewed failed sign-ins by IP address to identify whether the same IP was associated with multiple failed attempts. This can help detect suspicious external activity or repeated authentication failures from a single source.



\## Query 3 Findings

I reviewed Windows failed logon events using SecurityEvent Event ID 4625 to identify accounts and systems with repeated failed authentication attempts.



\## Query 4 Findings

I reviewed repeated failed Windows logons by account to identify accounts with multiple failures over time. This supports further investigation into possible misuse or abnormal behaviour.



\## Query 5 Findings

I reviewed Azure activity data to understand which operations and callers were most active in the environment.



\## Analyst Conclusion

The threat hunting exercise showed how Microsoft Sentinel can be used to proactively search for suspicious behaviour using KQL queries. Even where activity appears benign, the process improves analyst visibility and strengthens investigation skills.



\## Recommended Next Step

Continue monitoring suspicious authentication activity, improve KQL hunting skills, and correlate results with incidents or alerts where appropriate.

