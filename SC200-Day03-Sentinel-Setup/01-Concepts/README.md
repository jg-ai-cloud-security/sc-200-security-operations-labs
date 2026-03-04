\# Sentinel Data Ingestion Concepts



\## Overview



Microsoft Sentinel collects security telemetry from multiple sources including:



\- Azure resources

\- On-premise servers

\- Multi-cloud environments

\- Network devices

\- Security products



In this lab we implemented a \*\*hybrid log ingestion architecture\*\* using Azure Arc and Azure Monitor Agent.



---



\## Key Components



\### Azure Arc



Azure Arc allows \*\*non-Azure machines\*\* such as:



\- VMware servers

\- Physical servers

\- Other cloud VMs



to be managed as Azure resources.



This allows centralized monitoring, security policy enforcement, and telemetry collection.



---



\### Azure Connected Machine Agent



The Azure Connected Machine Agent is installed on machines onboarded through Azure Arc.



Responsibilities:



\- Registers the machine in Azure

\- Enables Azure management capabilities

\- Allows monitoring extensions to be deployed



---



\### Azure Monitor Agent (AMA)



The Azure Monitor Agent collects telemetry from the operating system including:



\- Windows Security Events

\- Linux Syslog logs

\- Performance metrics



This data is sent to Azure Monitor and Log Analytics.



---



\### Data Collection Rules (DCR)



Data Collection Rules define:



\- Which machines send logs

\- Which log types are collected

\- Where the data is sent



This allows precise control over log ingestion.



---



\### Log Analytics Workspace



The Log Analytics workspace acts as the \*\*central storage location\*\* for logs before they are analyzed by Microsoft Sentinel.



Logs stored here can be queried using \*\*Kusto Query Language (KQL)\*\*.



---



\### Microsoft Sentinel



Microsoft Sentinel is a \*\*cloud-native SIEM and SOAR platform\*\* used to:



\- Detect threats

\- Investigate incidents

\- Automate security response

\- Perform threat hunting

