

Content:



```markdown

\# SC-200 Day 03 Architecture



\## Hybrid Log Ingestion Architecture



This lab demonstrates how security logs from hybrid infrastructure are ingested into Microsoft Sentinel.



The environment consists of two virtual machines running in a VMware environment:



Windows Server



SC200-WIN-SEC01  

Windows Server 2025  

Security Events



Linux Server



SC200-LINUX-SEC01  

Ubuntu 24.04  

Syslog authentication logs



Both machines are onboarded into Azure using Azure Arc.



The Azure Monitor Agent collects system logs and sends them to Azure Monitor.



A Data Collection Rule determines which logs are collected and routes them to the Log Analytics workspace.



Microsoft Sentinel then ingests the logs for security monitoring and investigation.



---



\## Architecture Diagram



!\[Sentinel Architecture](SC200-Day03-Sentinel-Hybrid-Log-Ingestion-Architecture.png)



---



\## Key Technologies



Azure Arc  

Azure Monitor Agent  

Data Collection Rules  

Log Analytics Workspace  

Microsoft Sentinel  

VMware  

Windows Server 2025  

Ubuntu Linux

