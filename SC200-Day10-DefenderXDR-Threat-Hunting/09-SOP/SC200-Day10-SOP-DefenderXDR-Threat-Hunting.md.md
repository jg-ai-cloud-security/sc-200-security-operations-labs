\# SC-200 Day 10 SOP — Microsoft Defender XDR Threat Hunting Procedure



\## Purpose

This SOP defines the standard process for using Microsoft Defender XDR Advanced Hunting to investigate suspicious activity and support SOC operations.



\## Scope

This procedure applies to security analysts responsible for reviewing endpoint, identity, email, and alert telemetry in Microsoft Defender XDR.



\## Business Context

BrightSpark Electrical Services Ltd requires improved proactive threat visibility across its Microsoft security environment. The business needs a repeatable process for identifying suspicious activity early and supporting faster security investigation.



\## Tools Used

\- Microsoft Defender XDR

\- Advanced Hunting

\- Kusto Query Language (KQL)



\## Procedure

1\. Sign in to the Microsoft Defender portal.

2\. Open the Advanced Hunting experience.

3\. Review the available schema tables.

4\. Select the relevant telemetry source such as endpoint, identity, email, or alert data.

5\. Run approved KQL hunting queries.

6\. Review the returned results for suspicious behaviour, indicators, or anomalies.

7\. Record key findings in the investigation notes.

8\. Determine whether escalation or response action is required.

9\. Document lessons learned and possible detection improvements.



\## Expected Outcome

Analysts can proactively investigate suspicious behaviour by querying raw telemetry and validating findings before threats escalate further.



\## Business Value

This SOP helps the business improve threat visibility, standardize investigation steps, reduce response delays, and strengthen SOC maturity.



\## Review Notes

This SOP should be reviewed and updated as new telemetry sources, hunting queries, or investigation requirements are introduced.

