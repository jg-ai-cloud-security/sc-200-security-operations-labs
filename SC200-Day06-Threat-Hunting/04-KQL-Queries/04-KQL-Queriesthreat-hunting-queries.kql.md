// Query 1 - Failed sign-in attempts

SigninLogs

| where ResultType != 0

| summarize FailedAttempts = count() by UserPrincipalName, IPAddress

| order by FailedAttempts desc



// Query 2 - High sign-in activity by IP

SigninLogs

| summarize LoginCount = count() by IPAddress

| order by LoginCount desc



// Query 3 - Multiple IPs per user

SigninLogs

| summarize LoginIPs = dcount(IPAddress) by UserPrincipalName

| where LoginIPs > 3

