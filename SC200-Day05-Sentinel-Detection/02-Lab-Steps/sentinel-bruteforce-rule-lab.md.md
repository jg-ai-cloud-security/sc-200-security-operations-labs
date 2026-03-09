\# SC-200 Day 05 Lab — Brute Force Detection Rule



\## Objective



Create a detection rule in Microsoft Sentinel that identifies brute force login attempts using KQL queries.



\## Environment



Microsoft Sentinel  

Log Analytics Workspace: law-sc200-sentinel



---



\## Step 1 — Open Microsoft Sentinel



1\. Open Azure Portal

2\. Navigate to Microsoft Sentinel

3\. Select your Log Analytics workspace



---



\## Step 2 — Run Detection Query



Open Logs and run the following query:


## Lab Note

This lab focuses on building detection logic using KQL queries and analytics rules.

Because the environment does not currently ingest Windows Security Event logs, the query may return no results.

In production environments the query would detect repeated failed login attempts and generate security alerts.


```kql

SecurityEvent

| where EventID == 4625

| summarize FailedAttempts = count() by Account, Computer, bin(TimeGenerated, 5m)

| where FailedAttempts > 5



## Step 5 — Automated Response

The automated response stage allows security teams to trigger playbooks that automatically respond to security alerts.

Examples of automated actions include:

• Blocking malicious IP addresses  
• Disabling compromised user accounts  
• Sending alerts to security teams  
• Creating incident tickets

For this lab no playbook was configured. The analytics rule was created without automation to focus on detection and incident generation in Microsoft Sentinel.


## Lab Outcome

A Microsoft Sentinel analytics rule was successfully created to detect repeated failed login attempts using Windows Security EventID 4625.

The rule monitors authentication logs and generates incidents when suspicious activity is detected. This demonstrates how SOC teams implement detection engineering within a SIEM platform.




