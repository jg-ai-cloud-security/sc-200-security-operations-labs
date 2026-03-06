# Microsoft Sentinel Analytics Rules

Microsoft Sentinel analytics rules are used to detect suspicious or malicious activity by analyzing security logs collected in the Log Analytics workspace.

These rules use Kusto Query Language (KQL) to identify patterns that may indicate security threats such as brute force login attempts, privilege escalation, or suspicious network activity.

When a detection rule is triggered, Microsoft Sentinel automatically creates a security incident which can be investigated by security analysts.

## Key Technologies

- Microsoft Sentinel
- Azure Monitor Agent (AMA)
- Log Analytics Workspace
- Kusto Query Language (KQL)

## Detection Example

This lab focuses on detecting multiple failed login attempts which may indicate a brute-force attack.