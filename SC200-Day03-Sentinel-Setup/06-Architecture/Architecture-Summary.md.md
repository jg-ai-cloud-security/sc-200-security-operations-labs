\# Architecture Summary — SC200 Day 03



\## Overview

This lab establishes a basic Security Operations Center (SOC)

monitoring architecture using Microsoft Sentinel.



\## Components

\- Entra ID: generates authentication logs

\- Log Analytics Workspace: centralized log storage

\- Microsoft Sentinel: SIEM platform

\- Analytics Rules: detect suspicious behaviour



\## Security Flow

User authentication events are collected from Entra ID,

ingested into Log Analytics, analysed by Sentinel,

and converted into incidents for investigation.



\## Security Objective

Enable centralized detection and investigation

capability for identity-based threats.

