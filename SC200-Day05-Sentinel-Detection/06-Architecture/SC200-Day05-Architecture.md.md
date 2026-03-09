\# SC-200 Day 05 — Sentinel Detection Architecture



\## Overview



This architecture demonstrates how Windows security logs are collected and analyzed by Microsoft Sentinel to detect brute force authentication attempts.



\## Data Flow



Windows Server  

↓  

Azure Arc Agent  

↓  

Log Analytics Workspace  

↓  

Microsoft Sentinel  

↓  

Analytics Rule (KQL Detection)  

↓  

Security Alert  

↓  

Incident  

↓  

SOC Investigation



\## Security Value



This detection pipeline allows SOC teams to monitor authentication activity and automatically generate incidents when suspicious login behavior is detected.

