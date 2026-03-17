SecurityIncident

| take 10



SecurityAlert

| take 10



SecurityIncident

| project TimeGenerated, Title, Severity, Status, Owner

| take 10

