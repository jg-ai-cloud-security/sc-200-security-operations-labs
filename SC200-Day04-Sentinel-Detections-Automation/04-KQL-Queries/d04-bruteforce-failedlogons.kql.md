SecurityEvent

| where EventID == 4625

| summarize FailedAttempts=count() by Account, IpAddress, Computer

| where FailedAttempts >= 5

