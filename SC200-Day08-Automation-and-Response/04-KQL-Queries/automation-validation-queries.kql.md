// SC-200 Day 08 - Automation Validation Queries



SecurityIncident

| take 10



SecurityAlert

| take 10



SecurityIncident

| project TimeGenerated, IncidentNumber, Title, Severity, Status, Owner

| take 10

