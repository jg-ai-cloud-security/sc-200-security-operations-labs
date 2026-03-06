# Architecture Explanation

This architecture demonstrates how Microsoft Sentinel collects and analyzes security telemetry from hybrid environments.

Windows and Linux servers send security logs to Azure Monitor using the Azure Monitor Agent (AMA). These logs are stored in the Log Analytics workspace where Microsoft Sentinel performs security analysis using KQL queries.

Analytics rules continuously monitor incoming security events and automatically generate incidents when suspicious activity is detected.

This architecture enables centralized security monitoring, threat detection, and incident response capabilities for organizations without requiring traditional on-premise SIEM infrastructure.