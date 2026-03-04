# Azure Arc Onboarding Lab

## Objective

Onboard on-premise machines hosted in VMware into Azure using Azure Arc and configure them to send logs to Microsoft Sentinel.

---

## Step 1 — Deploy Virtual Machines

Two virtual machines were created in VMware:

Windows Server:

SC200-WIN-SEC01  
Windows Server 2025

Linux Server:

SC200-LINUX-SEC01  
Ubuntu 24.04

---

## Step 2 — Onboard Machines Using Azure Arc

Navigate to:

Azure Portal → Azure Arc → Machines → Add

Generate onboarding script.

Run script on each machine.

Windows:

PowerShell script executed as Administrator.

Linux:

Bash script executed in terminal.

Machines appear in Azure Arc once successfully connected.

---

## Step 3 — Install Azure Monitor Agent

Navigate to:

Azure Arc → Machines → Extensions

Install:

Azure Monitor Agent (AMA)

This enables telemetry collection from both machines.

---

## Step 4 — Create Data Collection Rule

Navigate to:

Azure Monitor → Data Collection Rules

Create rule:

dcr-sc200-securitylogs

Configure data sources:

Windows:

Security Events

Linux:

Syslog  
auth  
authpriv

---

## Step 5 — Attach Machines to Data Collection Rule

Add both machines as targets:

SC200-WIN-SEC01  
SC200-LINUX-SEC01

Destination:

Log Analytics Workspace

law-sc200-sentinel-jg

---

## Step 6 — Validate Log Ingestion

Open Microsoft Sentinel → Logs

Test queries.

Windows:

SecurityEvent

Linux:

Syslog