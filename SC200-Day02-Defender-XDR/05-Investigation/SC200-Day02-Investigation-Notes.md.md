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
- What went well:
- What to improve tomorrow:
- Tomorrow goal: onboard endpoint / enable signal sources and re-test hunting tables