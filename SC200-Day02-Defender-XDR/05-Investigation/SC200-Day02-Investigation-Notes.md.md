# SC-200 Day 02 — Investigation Notes (Defender XDR)

## Summary
- No alerts/incidents available in Defender XDR at this time.
- Investigation completed using portal validation + Advanced Hunting schema/queries.
- Next step: onboard a device / enable signal sources to generate richer telemetry and alerts.

---

## Incident Details
- Incident title: N/A (no incidents available)
- Incident ID: N/A
- Severity: N/A
- Status: N/A
- Created time: N/A
- Alerts count: 0

## Advanced Hunting Schema Findings
- `DeviceInfo` table not available (semantic error).
- Available tables confirmed:
  - AlertEvidence
  - BehaviorEntities
  - BehaviorInfo

---

## Evidence Collected
- SC200-Day02-01-DefenderXDR-Portal-Home.png
- SC200-Day02-02-DefenderXDR-Alerts-0.png
- SC200-Day02-03-DefenderXDR-Incidents-0.png
- SC200-Day02-04-AdvancedHunting-Schema-DeviceTables.png
- SC200-Day02-06-AdvancedHunting-Query01-Results.png
- SC200-Day02-07-AdvancedHunting-Query02-Results.png

## KQL Used
- SC200-Day02-Hunting-Query01.kql
- SC200-Day02-Hunting-Query02.kql

---

## Advanced Hunting Findings
### Query 01 Results (summary)
- Key result(s):
- Notes / interpretation:

### Query 02 Results (summary)
- Key result(s):
- Notes / interpretation:

---

## Analyst Decision
- Classification: Baseline validation / No telemetry
- Reason: No alerts/incidents available; hunting schema shows limited tables.
- Actions taken:
  - Documented current state and limitations
  - Captured evidence screenshots
  - Saved hunting queries

## Lessons Learned

• How Defender XDR investigation flows from signals → alerts → incidents → entity pivots → hunting → response.
• Why some KQL tables (like DeviceInfo) may not exist if Defender for Endpoint isn’t onboarded.
• How to use Schema in Advanced Hunting to confirm what telemetry is available.
How to document SOC work even when there are 0 alerts/incidents (baseline validation is still a real SOC task

- What went well:

• Created SC200 Day 02 folder structure using your standard template.
• Built Diagram 01: Defender XDR Investigation Flow (signals → incidents → hunting → response).
• Captured evidence of tenant state and hunting schema availability.
Created Day 02 documentation:

- What to improve tomorrow:
Enable telemetry/onboard endpoint for real incident

- Tomorrow goal: onboard endpoint / enable signal sources and re-test hunting tables