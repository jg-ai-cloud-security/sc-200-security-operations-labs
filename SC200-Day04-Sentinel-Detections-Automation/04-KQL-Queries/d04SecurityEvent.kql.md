SecurityEvent

| summarize count() by EventID

| order by count\_ desc

