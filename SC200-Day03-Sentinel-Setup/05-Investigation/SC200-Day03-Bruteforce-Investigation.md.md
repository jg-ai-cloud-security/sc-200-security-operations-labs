# Log Ingestion Validation

## Objective

Verify that Windows and Linux security logs are successfully ingested into Microsoft Sentinel.

---

## Windows Security Events

Query:

```kql
SecurityEvent
| take 10