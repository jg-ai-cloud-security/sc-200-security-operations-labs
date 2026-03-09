\# SC-200 Day 05 — Sentinel Detection Engineering



\## Overview



Detection engineering is the process of creating detection rules that identify suspicious or malicious activity in security telemetry. In Microsoft Sentinel, detection logic is implemented using KQL queries and scheduled analytics rules.



\## Key Concepts



\### Microsoft Sentinel Analytics Rules

Analytics rules run KQL queries against ingested logs to detect suspicious activity and generate alerts or incidents.



\### Scheduled Analytics Rule

A rule that runs at a defined interval and evaluates log data over a selected time window.



\### Security Alert

An alert is generated when detection logic identifies suspicious activity.



\### Security Incident

An incident groups alerts together to help SOC analysts investigate and respond to threats.



\### Brute Force Attack

A brute force attack occurs when an attacker repeatedly attempts to log in using different passwords to gain access to an account.



\## Detection Engineering Workflow



Logs → KQL Query → Analytics Rule → Alert → Incident → Investigation

