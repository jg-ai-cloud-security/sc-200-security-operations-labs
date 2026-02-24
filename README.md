\# SC-200 — Microsoft Security Operations Analyst (SOC Labs)



This repository documents my \*\*hands-on learning journey\*\* for the \*\*Microsoft SC-200 (Security Operations Analyst Associate)\*\* certification.



These labs are built to reflect \*\*real SOC work\*\*: onboarding data sources, investigating incidents, threat hunting with KQL, detection engineering, and automating response with Sentinel + Defender XDR.



\*\*Author:\*\* Jose Garcia  

\*\*Brand:\*\* JG AI Cloud Security



---



\## What You’ll Find Here



\- SOC-style labs with \*\*evidence\*\* (screenshots, notes, and investigation timelines)

\- \*\*KQL hunting queries\*\* and detection logic (MITRE-aligned where possible)

\- \*\*Microsoft Sentinel\*\* workbooks, analytics rules, and automation rules

\- \*\*Defender XDR\*\* incident investigation (alerts → incidents → entities → response)

\- Portfolio-ready structure to show consistent, repeatable SOC capability



---



\## Objectives



\- Deploy and configure \*\*Microsoft Sentinel SIEM\*\*

\- Connect data sources (M365, Entra ID, Defender XDR, Azure activity, endpoints)

\- Investigate and triage incidents using \*\*Defender XDR + Sentinel\*\*

\- Perform threat hunting using \*\*KQL\*\*

\- Build and tune \*\*analytics rules\*\* and detections

\- Automate security response workflows (Sentinel automation + Logic Apps playbooks)

\- Build SOC reporting: workbooks, dashboards, and operational runbooks



---



\## Skills Demonstrated



\- SOC operations workflow (triage, investigation, containment, remediation)

\- Incident investigation (entities, timelines, correlated alerts)

\- Threat hunting and query development (KQL)

\- Detection engineering (rules, tuning, suppression, MITRE mapping)

\- SIEM/SOAR configuration (connectors, workbooks, playbooks)

\- Security monitoring and alerting strategy

\- Documentation discipline (evidence, runbooks, lessons learned)



---



\## Labs Index



> Each folder represents one operational lab day and contains: Concepts, Lab steps, Screenshots, KQL, Architecture notes, and Lessons Learned.



\- \[Day 00 — SOC Lab Foundation (Sentinel Setup + Baseline)](./SC-200Day-00-SOC-Lab-Foundation/)

\- \[Day 01 — Data Connectors + Ingestion Validation](./SC-200Day-01-Data-Connectors-Ingestion/)

\- \[Day 02 — Incident Investigation (Sentinel + Defender XDR)](./SC-200Day-02-Incident-Investigation/)

\- \[Day 03 — KQL Threat Hunting Core Queries](./SC-200Day-03-KQL-Threat-Hunting/)

\- \[Day 04 — Detection Engineering (Analytics Rules + MITRE)](./SC-200Day-04-Detection-Engineering/)

\- \[Day 05 — SOAR Automation (Automation Rules + Playbooks)](./SC-200Day-05-SOAR-Automation/)

\- \[Day 06 — Workbooks + SOC Reporting](./SC-200Day-06-Workbooks-Reporting/)

\- \[Day 07 — Capstone SOC Scenario (End-to-End)](./SC-200Day-07-Capstone-EndToEnd/)



\*(Update folder links as your repo grows.)\*



---



\## SOC Baseline Used Across This Repo



\- Centralize logs in \*\*Log Analytics + Sentinel\*\*

\- Use \*\*least privilege RBAC\*\* for SOC roles

\- Validate ingestion before building detections

\- Map detections to \*\*MITRE ATT\&CK\*\*

\- Tune alerts (reduce noise, add suppression, improve fidelity)

\- Automate repeatable actions (enrichment, notifications, containment steps)

\- Maintain evidence and investigation notes for audit-ready documentation



---



\## How To Use This Repo



1\. Start with \*\*Day 00 — SOC Lab Foundation\*\*

2\. Follow the day README + `/02-Lab-Guide/`

3\. Use `/04-KQL/` for hunting queries and `/07-Analytics-Rules/` for detections

4\. Review `/05-Incidents/` for investigation workflow evidence

5\. Use `/08-Automation/` for playbooks and response workflows



---



\## Cost Hygiene



To avoid unnecessary charges:

\- Start small and expand ingestion sources gradually

\- Use budgets + alerts

\- Disable connectors you’re not testing

\- Remove test rules/playbooks when done

\- Delete lab resources after evidence capture (if not needed)



---



\## Disclaimer



This repository is for learning and portfolio demonstration.  

All sensitive values are masked in screenshots. Tenant/resource names may vary per environment.

