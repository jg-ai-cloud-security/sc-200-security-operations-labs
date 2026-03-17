\# SC200 Day 09 Architecture



\## Overview



This architecture shows how Microsoft Sentinel can connect security monitoring with automated response by using playbooks built in Azure Logic Apps.



\## Architecture Flow



Security alert or incident is generated in Microsoft Sentinel.  

The alert or incident can be reviewed by the SOC analyst.  

A playbook is used to trigger a response workflow.  

The playbook runs in Azure Logic Apps.  

The workflow performs an action such as sending an email notification.  

This creates a faster and more consistent response process in the SOC.



\## Components



\### Microsoft Sentinel

Microsoft Sentinel provides the security monitoring platform where alerts and incidents are detected, investigated, and managed.



\### Playbook

The playbook acts as the response workflow that connects Sentinel to automated actions.



\### Azure Logic Apps

Azure Logic Apps provides the workflow engine used to run the playbook steps.



\### Response Action

In this lab, the response action reviewed was \*\*Send an email (V2)\*\*, which shows how Sentinel can automate notification-based response.



\## Trigger Reviewed



The playbook reviewed in this lab used the \*\*Microsoft Sentinel alert\*\* trigger.



\## Action Reviewed



The workflow action reviewed in this lab was \*\*Send an email (V2)\*\*.



\## What This Diagram Proves



This diagram proves that Microsoft Sentinel can use playbooks and Azure Logic Apps to automate response actions after an alert or incident is identified. It also shows how SOC teams can reduce manual effort and improve consistency by using workflow-based response.



\## Why It Matters



This matters because security teams need a repeatable and efficient way to respond to threats. Playbooks help standardize actions, improve operational speed, and support better SOC response processes.



\## Day 09 Conclusion



Day 09 showed how Microsoft Sentinel playbooks support threat response by linking alerts or incidents to automated workflows in Azure Logic Apps. This strengthens understanding of Sentinel SOAR capabilities and real-world security operations.

