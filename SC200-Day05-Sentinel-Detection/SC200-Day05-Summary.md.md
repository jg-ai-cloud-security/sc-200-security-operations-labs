# SC-200 Day 05 — Sentinel Detection Engineering

## Overview

Today I focused on implementing detection engineering in Microsoft Sentinel by creating a scheduled analytics rule to detect brute-force login attempts using KQL queries.

This lab demonstrates how SOC analysts transform detection logic into automated alerts and incidents that can be investigated within the Sentinel platform.

---

## Business Scenario

BrightSpark Electrical Services Ltd is a small electrical contractor company whose employees remotely access company systems and cloud services.

The organisation recently implemented Microsoft Sentinel to improve security monitoring and gain visibility into authentication activity across their environment.

---

## Business Problem

Without centralized monitoring, repeated failed login attempts targeting employee accounts could go unnoticed. This increases the risk of brute-force attacks that may lead to unauthorized system access.

The company needs automated detection capabilities to identify suspicious authentication behaviour.

---

## Security Solution

Microsoft Sentinel provides centralized monitoring of authentication events. By creating analytics rules powered by KQL queries, the SOC team can automatically detect repeated failed login attempts and generate incidents for investigation.

---

## Security Benefits

• Early detection of credential attack attempts  
• Centralized monitoring of authentication events  
• Automated incident creation for SOC investigation  
• Improved visibility of suspicious login activity

---

## Objectives

Create and test a KQL query to detect failed login attempts

Convert the query into a Scheduled Analytics Rule

Enable incident creation and entity mapping

Document detection workflow and architecture

---

## What I Built

### Detection (KQL)

Brute force login detection using Windows Security Event logs.

Query detects repeated failed logon attempts within a short timeframe.

Saved in:

/04-KQL-Queries/bruteforce-detection.kql

---

### Analytics Rule

Scheduled query rule created in Microsoft Sentinel.

Configuration:

Run frequency: 5 minutes  
Lookback window: 5 minutes  
Alert threshold: results greater than 0

Features enabled:

Entity mapping (Account / Host)

Incident creation enabled

---

### Investigation

KQL query executed successfully in Sentinel Logs.

Due to the lab environment not generating Windows Security Event logs, no results were returned. However, the detection rule was correctly configured and validated.

---

### Architecture

Detection workflow implemented:

Log Sources  
↓  
Log Analytics Workspace  
↓  
Microsoft Sentinel  
↓  
KQL Detection Query  
↓  
Scheduled Analytics Rule  
↓  
Alert  
↓  
Incident  
↓  
SOC Investigation

Architecture documentation stored in:

/06-Architecture

---

## Evidence (Screenshots)

Stored in:

/03-Evidence

SC200-Day05-01-KQL-BruteforceQuery.png  
SC200-Day05-02-AnalyticsRule-Created.png  
SC200-Day05-03-RuleLogic-Configured.png  
SC200-Day05-04-IncidentSettings-Configured.png  
SC200-Day05-05-AnalyticsRules-List.png

---

## Challenges / Notes

The lab environment does not generate Windows Security Event logs, therefore the detection query returned no results.

This scenario is common in lab environments and does not affect the validity of the detection logic implemented.

---

## Key Takeaways

Detection engineering is a critical SOC capability that converts threat detection logic into automated alerts.

Scheduled analytics rules allow SOC teams to continuously monitor log data and detect suspicious behaviour.

Entity mapping enriches alerts with contextual information such as user accounts and host systems.

---

## Next Steps (Day 06)

Perform threat hunting using KQL queries

Investigate suspicious authentication patterns

Build advanced hunting queries to detect anomalies in authentication logs