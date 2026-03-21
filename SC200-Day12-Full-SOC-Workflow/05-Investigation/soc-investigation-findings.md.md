\# SC-200 Day 12 Investigation Findings



\## Investigation Summary



This lab focused on reviewing a full SOC workflow in Microsoft Sentinel and Microsoft Defender XDR.



The environment was reviewed for incidents, alerts, entity relationships, KQL log analysis, automation, and Defender integration.



\## Observations



\- Microsoft Sentinel workspace was accessible

\- Incidents and alerts were reviewed

\- Investigation graph was examined

\- KQL queries were used to validate available data

\- Automation rules and playbooks were reviewed

\- Microsoft Defender portal was accessible

\- No active Defender incidents or alerts were present during the lab



\## Defender XDR Integration



No active incidents or alerts were observed in Microsoft Defender during this lab.



This indicates that while the Defender environment is accessible, there is currently no active security activity being generated or ingested for investigation.



In a production environment, Defender would generate alerts that could be forwarded to Microsoft Sentinel for centralized SOC investigation.



\## AI-Assisted Investigation



AI functionality was simulated based on Microsoft Security Copilot capabilities.



The simulated AI workflow was used to:

\- summarize the incident context

\- identify what appeared suspicious

\- recommend next investigation steps



All outputs were validated manually using Sentinel data and available logs.



\## Conclusion



This lab demonstrates the expected SOC workflow:

Detection → Investigation → Validation → Response



Even with limited live data, the full process and tool relationships were successfully reviewed and documented.

