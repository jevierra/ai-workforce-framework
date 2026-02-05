# Service & Maintenance Specialist - Brain

## Service Call Tracking

### Status Categories

| Status | Definition |
|--------|-----------|
| **Open** | Reported but not yet assigned or in progress |
| **In Progress** | Technician assigned, actively being worked |
| **Waiting on Parts** | Diagnosed, requires parts order |
| **Waiting on Customer** | Requires customer action (access, information, approval) |
| **Escalated** | Beyond standard support, requires specialist or vendor involvement |
| **Resolved** | Issue fixed, pending customer confirmation |
| **Closed** | Confirmed resolved, ticket complete |

### Priority Levels

| Priority | Response Time | Description |
|----------|--------------|-------------|
| **Critical** | 4 hours | System down, no workaround, business impact |
| **High** | 8 hours | Major functionality impaired, limited workaround |
| **Medium** | 24 hours | Functionality impaired, workaround available |
| **Low** | 48 hours | Minor issue, no business impact |

### Tracking Discipline
- Every call gets logged. Every. Single. One.
- Status updates at minimum every 24 hours for open calls
- Time-to-resolution tracked for SLA compliance
- Recurring issues flagged after second occurrence on same device/account
- Chronic accounts (3+ calls in 30 days) escalated for review

---

## Maintenance Contract Monitoring

### Contract Lifecycle
1. **Active** - Under coverage, all services available
2. **Expiring** - Within 90 days of expiration (flag for renewal)
3. **Expired** - Coverage lapsed, service at time-and-materials rates
4. **Pending Renewal** - Renewal quote issued, awaiting signature

### What to Track
- Contract start and end dates
- Coverage level (parts, labor, consumables, response time guarantees)
- Equipment covered under each contract
- Usage vs. allocation (are they over/under their included volume?)
- Renewal history (have they renewed consistently or do they lapse?)

### Renewal Alerting
- **90 days out:** Flag for sales team, begin renewal preparation
- **60 days out:** Renewal quote should be issued
- **30 days out:** If unsigned, escalate
- **Expired:** Alert immediately, note service coverage gap

---

## Software Troubleshooting

### Document Management Issues
- User access/permissions problems
- Workflow routing failures
- Search/retrieval errors
- Integration failures with line-of-business apps
- Storage and performance issues

### Print Management Issues
- Print queue failures
- Driver conflicts
- Authentication/secure print release failures
- Cost tracking discrepancies
- Fleet communication errors

### Scanning Solutions Issues
- OCR accuracy problems
- Index field mapping errors
- Destination routing failures
- Image quality issues
- Batch processing failures

### Troubleshooting Protocol
1. **Reproduce** - Can we recreate the issue?
2. **Isolate** - Is it user-specific, device-specific, or systemic?
3. **Diagnose** - What changed? New update? New user? New configuration?
4. **Resolve** - Fix the root cause, not just the symptom
5. **Document** - Log everything. What happened, why, how it was fixed, how to prevent it.

---

## Pattern Analysis

### What to Look For

**Device Patterns**
- Same device generating repeated calls = potential replacement candidate
- Same error code across multiple devices = systemic issue (firmware, configuration, environment)

**Account Patterns**
- Chronic high-call accounts = possible training gap, environmental issue, or wrong solution deployed
- Seasonal spikes = predictable, can be proactively managed

**Issue Patterns**
- Same issue across multiple accounts after a software update = update problem
- Gradual increase in call volume = capacity or aging equipment issue
- Sudden spike = event-driven (update, environmental change, user error)

### Reporting Cadence
- **Daily:** Open call count, critical items, SLA status
- **Weekly:** Trend summary, chronic accounts, aged tickets
- **Monthly:** Full service analysis, pattern report, contract status
- **Quarterly:** Strategic review - what's working, what's failing, what needs to change
