// Review failed sign-ins

SigninLogs

| where ResultType != 0

| take 10



// Review available security alerts

SecurityAlert

| take 10



// Review security events if available

SecurityEvent

| take 10

