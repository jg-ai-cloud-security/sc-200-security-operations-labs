# Incident Investigation

## Incident Type
Brute Force Login Detection

## Detection Method
Microsoft Sentinel analytics rule monitoring Windows Security Event ID 4625.

## Investigation Steps

1. Identify source IP address generating failed login attempts.
2. Review targeted user accounts.
3. Analyze the number of failed authentication attempts.
4. Determine if login attempts originate from internal or external sources.

## Potential Impact

Repeated failed login attempts may indicate an attacker attempting to gain unauthorized access to the system through password guessing.

## Recommended Response

- Lock the affected account
- Investigate source IP address
- Implement account lockout policies
- Enable Multi-Factor Authentication