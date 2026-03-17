\# Playbook Response Findings



\## What I Reviewed



I reviewed Microsoft Sentinel playbooks and how they are used to support SOC threat response through Azure Logic Apps.



\## Trigger Observed



The playbook was designed to run either manually on a selected incident or automatically through an automation rule when an incident is created or updated.



\## Response Action Observed



The workflow included response actions such as notification, enrichment, ticketing, or other automated response steps depending on the playbook design.



\## Why It Matters



This is important because playbooks help SOC teams standardize incident response, reduce manual effort, and improve the speed and consistency of security operations.



\## Day 09 Summary







KQL validation result: I ran a KQL query against the SecurityIncident table and confirmed that incident records were present in the Microsoft Sentinel workspace. The results showed multiple incidents with visible timestamps, titles, severity, and status values, confirming that Sentinel incident data was available for validation.







Day 09 focused on understanding how Microsoft Sentinel connects incidents, automation rules, and playbooks into one response workflow. This showed how SOAR capabilities improve real-world incident handling.

