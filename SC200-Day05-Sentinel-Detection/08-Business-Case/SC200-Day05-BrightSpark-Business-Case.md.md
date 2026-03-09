\# SC-200 Day 05 — Sentinel Detection Engineering



\## Business Scenario



BrightSpark Electrical Services Ltd is a small electrical contractor company whose employees remotely access company systems and cloud services.



An organization collects Windows security logs from on-premises servers connected to Azure through Azure Arc.  

The SOC team uses Microsoft Sentinel to monitor authentication activity and detect suspicious login behavior across the environment.





\## Business Problem



The organization currently lacks automated detection mechanisms to identify brute force login attempts.  

Without detection rules, repeated failed login attempts may go unnoticed, increasing the risk of unauthorized access to systems.



\## Security Solution



Microsoft Sentinel provides centralized monitoring of authentication events and enables automated detection of brute-force login attempts using analytics rules powered by KQL queries.



\## Security Benefits



• Early detection of account compromise attempts



• Centralized log monitoring across systems



• Automated alert and incident generation



• Improved security visibility for small businesses



\## Lab Objective



Create a Sentinel analytics rule that detects repeated failed login attempts and generates incidents for SOC investigation.

