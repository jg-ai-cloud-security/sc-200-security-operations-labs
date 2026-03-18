\# SC-200 Day 11 Lab Guide

\## Microsoft Defender XDR Incident Investigation



\## Part 1 — Open the Defender Portal

\### Step 1

Sign in to the Microsoft Defender portal.



\### Step 2

From the left menu, open \*\*Incidents \& alerts\*\*.



\### Step 3

Click \*\*Incidents\*\*.



\### Step 4

Review the incident queue page.



\### Step 5

Take your first screenshot.



\*\*Screenshot name\*\*  

SC200-Day11-01-Defender-Incident-Queue.png



\---



\## Part 2 — Review an Incident

\### Step 6

Open one available incident from the queue.



\### Step 7

Review the incident name, severity, status, and classification fields.



\### Step 8

Check whether the incident includes multiple related alerts.



\### Step 9

Take a screenshot showing the incident overview.



\*\*Screenshot name\*\*  

SC200-Day11-02-Incident-Overview.png



\---



\## Part 3 — Review Alerts and Impacted Entities

\### Step 10

Open the alerts section inside the incident.



\### Step 11

Identify whether the activity is endpoint-focused, identity-focused, email-focused, or multi-domain.



\### Step 12

Review the impacted entities, such as devices, users, or mailboxes.



\### Step 13

Take a screenshot showing alerts and entities.



\*\*Screenshot name\*\*  

SC200-Day11-03-Alerts-and-Entities.png



\---



\## Part 4 — Investigate an Entity

\### Step 14

Select one available entity, such as a device or user account.



\### Step 15

Review the entity page and note related evidence or activity.



\### Step 16

Check whether the page shows recent alerts, timeline activity, or related assets.



\### Step 17

Take a screenshot of the entity investigation page.



\*\*Screenshot name\*\*  

SC200-Day11-04-Entity-Investigation.png



\---



\## Part 5 — Review Advanced Hunting

\### Step 18

Open \*\*Hunting\*\* and then \*\*Advanced hunting\*\*.



\### Step 19

Review the available schema tables.



\### Step 20

Run a simple query such as:



AlertInfo

| take 10



\### Step 21

If available, run another query such as:



AlertEvidence

| take 10



\### Step 22

Take a screenshot of the Advanced Hunting page.



\*\*Screenshot name\*\*  

SC200-Day11-05-Advanced-Hunting.png



\---



\## Part 6 — Review Response Options

\### Step 23

Return to the incident and check what response options are available.



\### Step 24

Review whether you can assign, classify, or update the incident.



\### Step 25

If available, note whether any action or remediation options appear for the entity.



\### Step 26

Take a screenshot showing response or incident management options.



\*\*Screenshot name\*\*  

SC200-Day11-06-Response-Options.png



\---



\## Part 7 — Record Findings

\### Step 27

Document what you observed in the incident.



\### Step 28

Record whether useful investigation data was available.



\### Step 29

Write whether the workflow was focused on endpoint, identity, email, or a combination.



\### Step 30

Document what this means in a real SOC workflow.

