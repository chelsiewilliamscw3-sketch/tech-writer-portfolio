# Runbook: BI Data Refresh

## Purpose
Provide step by step instructions to refresh and validate the BI dataset used by Finance dashboards.

## Trigger
- Scheduled at 6:00 AM CST daily
- Manual refresh before month-end close as needed

## Steps
1. Open Power BI Service → Datasets → `Finance_Prod`.
2. Click **Refresh Now**.
3. Verify completion in Refresh History (status = Succeeded).
4. Run quick validation:
   - Row counts match previous day ± 5%
   - Latest transaction date is within 24 hours
5. If failed, see **Incident Response**.

## Incident Response
- Capture failure code and time
- Retry once; if it fails again, open a ticket with logs
- Post update in the Finance channel

## Contacts
- BI On-call: bi-oncall@example.com
