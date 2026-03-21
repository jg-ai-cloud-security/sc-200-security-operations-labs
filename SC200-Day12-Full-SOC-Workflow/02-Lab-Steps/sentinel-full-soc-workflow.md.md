\# SC-200 Day 12 — Full SOC Workflow Lab Guide



\---



\## Part 1 — Open Microsoft Sentinel



\### Step 1

Sign in to the Azure Portal.



\### Step 2

Search for \*\*Microsoft Sentinel\*\*.



\### Step 3

Open your SC-200 Log Analytics Workspace.



\### Step 4

Take a screenshot.



\*\*Screenshot name\*\*

SC200-Day12-01-Sentinel-Overview.png



\---



\## Part 2 — Review Incidents



\### Step 5

In the left menu, click \*\*Incidents\*\*.



\### Step 6

Review available incidents.



\### Step 7

Select one incident.



\### Step 8

Review:

\- Severity

\- Status

\- Alerts

\- Entities



\### Step 9

Take a screenshot.



\*\*Screenshot name\*\*

SC200-Day12-02-Incident-Overview.png



\---



\## Part 3 — Investigate Alerts



\### Step 10

Opened the Microsoft Defender \*\*Alerts\*\* queue from \*\*Incidents \& alerts > Alerts\*\*.



\### Step 11

Reviewed the queue and confirmed that no alerts were available in the current tenant during the selected time range.



\### Step 12

Verified the following:

\- No alert details were available

\- No triggered rule was visible

\- No timestamped alert activity was present

\- The queue was empty for the selected \*\*1 Week\*\* period



\### Step 13

Confirmed that no active alert investigation could be performed because the environment did not contain current alert records.



\### Step 14

Took a screenshot of the empty Alerts queue.



\*\*Screenshot name\*\*  

SC200-Day12-03-No-Alerts-Queue.png

\---



\## Part 4 — Entity Investigation



\### Step 14

Inside the incident, open the \*\*Investigation graph\*\*.



\### Step 15

Review entities such as:

\- User

\- IP address

\- Device



\### Step 16

Click each entity and review details.



\### Step 17

Take a screenshot.



\*\*Screenshot name\*\*

SC200-Day12-04-Entity-Investigation.png



\---



\## Part 5 — Timeline Analysis



\### Step 18

Review the \*\*incident timeline\*\*.



\### Step 19

Identify sequence of events.



\### Step 20

Take a screenshot.



\*\*Screenshot name\*\*

SC200-Day12-05-Timeline.png



\---



\## Part 6 — Perform KQL Queries



\### Step 21

Go to \*\*Logs\*\* in Sentinel.



\### Step 22

Run a query (example):



SigninLogs

| where ResultType != 0

| take 10



\### Step 23

Review results.



\### Step 24

Take a screenshot.



\*\*Screenshot name\*\*

SC200-Day12-06-KQL-Query.png



\---



\## Part 7 — Review Automation



\### Step 25

Go to \*\*Automation\*\*.



\### Step 26

Review:

\- Automation rules

\- Playbooks



\### Step 27

Check if playbooks can:

\- Run automatically

\- Run manually



\### Step 28

Take a screenshot.



\*\*Screenshot name\*\*

SC200-Day12-07-Automation.png



\---



\## Part 8 — Validate Defender XDR Integration



\### Step 29

Review alerts originating from Microsoft Defender.



\### Step 30

Confirm integration between:

\- Defender XDR

\- Microsoft Sentinel



\### Step 31

Take a screenshot.



\*\*Screenshot name\*\*

SC200-Day12-08-Defender-Integration.png



\---



\## Part 9 — AI-Assisted Investigation (Simulated)



\### Step 32

Simulate Security Copilot usage.



\### Step 33

Ask:

\- “Summarize this incident”

\- “What is suspicious?”

\- “What should I investigate next?”



\### Step 34

Compare AI output with your investigation.



\### Step 35

Document findings.



\### Step 36

Take a screenshot (optional).



\*\*Screenshot name\*\*

SC200-Day12-09-AI-Investigation.png



\---



\## Part 10 — Record Findings



\### Step 37

Document:

\- What you observed

\- What was suspicious

\- What logs confirmed activity



\### Step 38

Record whether:

\- Data was useful

\- Investigation was successful



\---



\## Part 11 — Architecture



\### Step 39

Create architecture diagram showing:



User / Device

↓

Defender XDR

↓

Sentinel

↓

Analytics Rules

↓

Incident

↓

Investigation

↓

Automation

↓

Response



\---



\## Part 12 — Finalize Lab



\### Step 40

Upload:

\- Screenshots

\- KQL queries

\- Documentation



\### Step 41

Update GitHub repository.



\### Step 42

Update Excel tracker.



\### Step 43

Prepare LinkedIn project summary.

