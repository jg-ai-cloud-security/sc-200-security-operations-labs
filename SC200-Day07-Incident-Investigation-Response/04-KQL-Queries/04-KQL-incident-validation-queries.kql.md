// Query 1 - Security alerts

SecurityAlert

| sort by TimeGenerated desc

| take 10



// Query 2 - Sign-in activity

SigninLogs

| sort by TimeGenerated desc

| take 10



// Query 3 - Security events

SecurityEvent

| sort by TimeGenerated desc

| take 10



// Query 4 - Device events

DeviceEvents

| sort by TimeGenerated desc

| take 10

