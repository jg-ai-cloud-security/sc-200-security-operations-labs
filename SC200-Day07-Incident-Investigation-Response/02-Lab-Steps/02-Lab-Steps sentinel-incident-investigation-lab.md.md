# SC-200 Day 07 — Microsoft Sentinel Incident Investigation Lab

## Objective
Review and document the incident investigation workflow in Microsoft Sentinel, validate supporting evidence with KQL, and simulate SOC triage using a manual test incident.

## Prerequisites
- Microsoft Sentinel deployed
- Log Analytics workspace available
- Access to Azure Portal
- GitHub and Azure DevOps structure already prepared

## Lab Steps

### Step 1 — Open Microsoft Sentinel
Open the Azure portal and go to Microsoft Sentinel.

### Step 2 — Open Incidents
Navigate to the Incidents page and review the current incident queue.

### Step 3 — Confirm incident availability
Check whether live incidents are present in the workspace.

### Step 4 — Create a manual test incident
Because no live incidents were initially available, create a manual test incident to simulate the Day 07 investigation workflow.

### Step 5 — Review incident details
Open the test incident and review the available details such as severity, status, owner, and description.

### Step 6 — Review investigation workflow
Check whether alerts, entities, or investigation graph data are available. Document any limitations caused by manual incident creation.

### Step 7 — Prepare KQL validation
Open Logs and prepare KQL queries to validate supporting security telemetry.

### Step 8 — Capture evidence
Take screenshots of the incident queue, test incident, full details, and KQL validation results.

### Step 9 — Document findings
Record the business scenario, risk, security goal, investigation notes, and architecture explanation.

### Step 10 — Update project records
Update OneNote, GitHub, Azure DevOps, and the Excel tracker for Day 07.

## Lab Note
Because this lab used a manual test incident, alerts, entities, and investigation graph relationships may be limited. The focus of the exercise is to understand and document the incident investigation workflow.