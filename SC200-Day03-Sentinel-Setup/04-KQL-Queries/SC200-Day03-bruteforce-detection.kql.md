SecurityEvent

| where EventID == 4625

| summarize FailedAttempts = count()

by Account, IpAddress, Computer, bin(TimeGenerated, 5m)

| where FailedAttempts >= 5

| sort by FailedAttempts desc

