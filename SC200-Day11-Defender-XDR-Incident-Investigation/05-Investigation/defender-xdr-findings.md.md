\# Defender XDR Findings



\## What I Observed

I successfully accessed the Microsoft Defender portal and opened the Incidents page under Investigation \& response. The portal loaded correctly, but no incidents were available in the current tenant view.



\## Investigation Focus

This review was focused on platform navigation and workflow validation rather than a live incident investigation.



\## Useful Data Available

No active incidents were available for review. However, the incident queue page, filters, columns, and portal structure were visible and confirmed how analysts would access the investigation workflow.



\## SOC Meaning

In a real SOC, this would mean either no qualifying incidents were currently generated or the tenant does not yet have enough connected security activity to populate the queue. Analysts would then move to alerts, hunting, connected data sources, or asset review to continue validation.



\## Conclusion

Day 11 still reinforced how to access Microsoft Defender XDR, review the incident queue structure, and understand where incident investigation would take place when data becomes available.



No entity investigation page was available during this lab because the tenant had no active incidents or alerts. This prevented review of impacted users, devices, or other related entities.



