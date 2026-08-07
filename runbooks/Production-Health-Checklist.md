# Production Health Checklist

## 1. Purpose

This checklist provides a standard approach for verifying the health and stability of production applications.

Regular health checks help identify potential issues early and ensure that critical application components are operating normally.

The objective is to verify:

- Application availability
- System stability
- Dependency health
- Operational readiness

---

# 2. General Information

| Field | Details |
|---|---|
| Application Name | |
| Environment | Production |
| Health Check Date | |
| Performed By | |
| Review Status | |

---

# 3. Application Availability Check

Verify application accessibility:

- [ ] Application URL is accessible
- [ ] Application loads successfully
- [ ] Login functionality is working
- [ ] No unexpected error messages observed
- [ ] Critical business functions are available

---

# 4. Application Service Check

Verify application-related services:

- [ ] Required application services are running
- [ ] Windows services status verified (if applicable)
- [ ] Application pools are healthy
- [ ] Background processes are running
- [ ] No unexpected service restarts observed

---

# 5. Server Health Check

Review application server health:

## Resource Utilization

- [ ] CPU utilization is within acceptable range
- [ ] Memory utilization is within acceptable range
- [ ] Disk space availability checked
- [ ] Server uptime verified


## Operating System Checks

- [ ] No critical system events
- [ ] No unexpected service failures
- [ ] System time synchronization verified

---

# 6. Database Health Check

Verify database availability and performance:

- [ ] Database connectivity verified
- [ ] Database server availability checked
- [ ] Storage capacity reviewed
- [ ] Failed connections reviewed
- [ ] Long-running queries checked
- [ ] Blocking/deadlock issues reviewed

---

# 7. Integration Health Check

Verify application dependencies:

- [ ] Internal API connectivity verified
- [ ] External API availability checked
- [ ] Message queues are processing successfully
- [ ] File transfer interfaces are working
- [ ] Third-party dependencies are available

---

# 8. Batch Job and Scheduler Check

Verify scheduled activities:

- [ ] Scheduled jobs completed successfully
- [ ] Failed jobs reviewed
- [ ] Processing delays checked
- [ ] Job output validated
- [ ] Failed executions investigated

---

# 9. Log Review

Review application and system logs:

Check for:

- [ ] Critical application errors
- [ ] Database errors
- [ ] Authentication failures
- [ ] Integration failures
- [ ] Repeated warnings


Important findings should be documented and tracked.

---

# 10. Monitoring and Alert Review

Review monitoring platforms:

- [ ] Active alerts reviewed
- [ ] Critical alerts investigated
- [ ] Dashboard status verified
- [ ] Performance trends reviewed
- [ ] Monitoring agents are healthy

---

# 11. Security and Access Checks

Verify security-related items:

- [ ] Certificates are valid
- [ ] Service accounts are working
- [ ] Access issues reviewed
- [ ] Security alerts checked
- [ ] Expiry notifications reviewed

---

# 12. Storage and File System Check

Verify storage availability:

- [ ] Application folders have sufficient space
- [ ] Log folders checked
- [ ] Temporary files reviewed
- [ ] File processing locations are available
- [ ] Backup locations are accessible

---

# 13. Health Check Findings

Record observations:

| Area | Status | Comments |
|---|---|---|
| Application | | |
| Services | | |
| Server | | |
| Database | | |
| Integrations | | |
| Jobs | | |
| Monitoring | | |

---

# 14. Escalation Guidelines

Escalate when:

- Application availability is impacted
- Critical alerts are triggered
- Database performance issues are detected
- Business-critical jobs fail
- Dependency systems are unavailable

Provide:

- Health check findings
- Error details
- Impact assessment
- Supporting evidence

---

# 15. Completion Checklist

- [ ] All health checks completed
- [ ] Issues identified and documented
- [ ] Required teams notified
- [ ] Health report shared
- [ ] Follow-up actions tracked

---

# 16. Best Practices

- Perform checks at defined intervals
- Focus on business-critical components
- Record observations consistently
- Track recurring health issues
- Review trends instead of only current status
- Update checklist based on application changes

---

**Document Purpose:** Production Environment Health Verification Checklist  
**Version:** 1.0
