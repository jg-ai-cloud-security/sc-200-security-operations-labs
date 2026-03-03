# SC-200 Day 02 — Microsoft Defender XDR (Investigation + Advanced Hunting)

## Objective
Use Microsoft Defender XDR to investigate an incident like a SOC analyst:
- Review incident and related alerts
- Investigate entities (user + device)
- Validate activity using Advanced Hunting (KQL)
- Document findings and closure decision

## Prerequisites
- Access to Microsoft Defender portal
- Permissions to view Incidents, Alerts, and Advanced Hunting
- Sample data or test telemetry available (recommended)

## Tools / Portals Used
- Microsoft Defender portal (Incidents & alerts)
- Advanced Hunting

---

## Step-by-Step Lab

### Step 1 — Confirm Defender XDR access
1. Sign in to Microsoft Defender portal.
2. Verify access to:
   - Incidents
   - Alerts
   - Advanced Hunting
3. Evidence:
   - SC200-Day02-01-DefenderXDR-Portal-Home.png

### Step 2 — Validate alerts/incidents state
1. Go to **Incidents & alerts > Alerts**
2. Change time range to **30–90 days**
3. Confirm current state (0 alerts expected in this tenant currently)
4. Go to **Incidents & alerts > Incidents**
5. Confirm current state (0 incidents expected currently)
6. Evidence:
   - SC200-Day02-02-DefenderXDR-Alerts-0.png
   - SC200-Day02-03-DefenderXDR-Incidents-0.png

### Step 3 — Confirm Advanced Hunting schema
1. Go to **Hunting > Advanced hunting**
2. Click **Schema**
3. Search `DeviceInfo` (not available in this tenant)
4. Confirm available tables:
   - AlertEvidence
   - BehaviorEntities
   - BehaviorInfo
5. Evidence:
   - SC200-Day02-04-AdvancedHunting-Schema-DeviceTables.png

### Step 4 — Run Advanced Hunting (KQL)
1. Run Query 01 and Query 02 (saved in `/04-KQL-Queries/`)
2. Capture results screenshots (even if empty)
3. Evidence:
   - SC200-Day02-06-AdvancedHunting-Query01-Results.png
   - SC200-Day02-07-AdvancedHunting-Query02-Results.png

### Step 5 — Document findings and next steps
1. Record investigation notes in `/05-Investigation/`
2. Note the tenant limitation (no alerts/incidents yet)
3. Document next step: onboard endpoint / enable signal sources

---

## Troubleshooting
- `DeviceInfo` query fails because the table is not available in this tenant's Advanced Hunting schema.
- Use tenant-supported tables: `AlertEvidence`, `BehaviorEntities`, `BehaviorInfo`.

## Results / Validation
- Validated Defender XDR access.
- Verified current alert/incident state (0 alerts/incidents in selected time range).
- Confirmed telemetry availability using Advanced Hunting (schema + supported tables).

---

## Validation Checklist
- [ ] Access confirmed to Defender XDR + Advanced Hunting
- [ ] Alerts/Incidents state validated (screenshots captured)
- [ ] Schema checked (DeviceInfo missing, supported tables confirmed)
- [ ] 2 hunting queries executed and saved
- [ ] Notes documented with limitations + next steps