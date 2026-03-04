\# SC-200 Day 03 — Microsoft Sentinel Hybrid Log Ingestion



\## Overview



In this lab I built a hybrid security monitoring architecture using Microsoft Sentinel.  

Two virtual machines were deployed in a VMware environment to simulate an on-premise infrastructure.



The machines were connected to Azure using Azure Arc and configured to send security logs to Microsoft Sentinel using the Azure Monitor Agent and Data Collection Rules.



This lab demonstrates how hybrid infrastructure can be monitored centrally using a cloud-native SIEM platform.



---



\# What I Learned



• How Azure Arc allows non-Azure machines to be managed as Azure resources.



• How the Azure Connected Machine Agent registers on-premise machines with Azure.



• How Azure Monitor Agent (AMA) collects system logs and telemetry.



• How Data Collection Rules define which logs are collected and where they are sent.



• How Microsoft Sentinel ingests Windows Security Events and Linux Syslog logs.



• How hybrid environments can be integrated into a centralized SOC monitoring platform.



---



\# What I Built Today



Hybrid security monitoring environment including:



VMware Infrastructure



• Windows Server 2025 VM  

SC200-WIN-SEC01



• Ubuntu Linux 24.04 VM  

SC200-LINUX-SEC01



Azure Components



• Azure Arc Connected Machines  

• Azure Monitor Agent (AMA)  

• Data Collection Rule (dcr-sc200-securitylogs)  

• Log Analytics Workspace (law-sc200-sentinel-jg)  

• Microsoft Sentinel SIEM



Log Sources Configured



Windows Logs



• SecurityEvent  

• EventID 4624 (Successful Login)  

• EventID 4625 (Failed Login)



Linux Logs



• Syslog  

• auth  

• authpriv



---



\# Architecture Implemented



VMware Servers  

↓  

Azure Arc Connected Machine Agent  

↓  

Azure Monitor Agent  

↓  

Data Collection Rule  

↓  

Log Analytics Workspace  

↓  

Microsoft Sentinel SIEM



---



\# Validation



Log ingestion was validated using KQL queries in Microsoft Sentinel.



Windows Query



```kql

SecurityEvent

| take 10

