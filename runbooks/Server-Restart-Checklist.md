# Server Restart Checklist

## 1. Purpose

This checklist provides a structured approach for performing server restarts safely in production environments.

A controlled restart helps restore application services while reducing the risk of unexpected impact.

The objective is to ensure:

- Proper planning before restart
- Controlled execution
- Successful application recovery
- Service availability after restart

---

# 2. Restart Scenarios

A server restart may be required for:

- Application service recovery
- Memory/resource cleanup
- Operating system maintenance
- Configuration changes
- Patch activities
- Infrastructure activities

A restart should only be performed after understanding the impact.

---

# 3. Pre-Restart Checklist

## Approval and Communication

- [ ] Restart activity is approved
- [ ] Maintenance window is confirmed
- [ ] Stakeholders are informed
- [ ] Responsible engineer is assigned
- [ ] Support coverage is available


## Impact Assessment

Verify:

- [ ] Affected application identified
- [ ] Business impact understood
- [ ] Dependent services identified
- [ ] User impact communicated


## Application Health Check

Before restart:

- [ ] Application status captured
- [ ] Current errors reviewed
- [ ] Active transactions checked
- [ ] Critical jobs verified
- [ ] Current monitoring status recorded

---

# 4. Backup and Recovery Validation

Before restart:

- [ ] Required backups are available
- [ ] Configuration changes are documented
- [ ] Recovery steps are known
- [ ] Support contacts are available

---

# 5. Restart Preparation

Before initiating restart:

- [ ] Confirm correct server
- [ ] Verify active user sessions
- [ ] Stop required application services (if needed)
- [ ] Ensure pending processing is completed
- [ ] Notify users if downtime is expected

---

# 6. Restart Execution Checklist

## Server Restart

- [ ] Initiate approved restart activity
- [ ] Monitor restart progress
- [ ] Confirm server availability
- [ ] Verify operating system startup completion


## Service Startup

After server restart:

- [ ] Required Windows services are running
- [ ] Application services are started
- [ ] Application pools are running
- [ ] Scheduled processes are available

---

# 7. Post-Restart Validation

## Application Validation

- [ ] Application URL is accessible
- [ ] User login works
- [ ] Critical functionality validated
- [ ] Application response is normal


## Technical Validation

Verify:

- [ ] Server resources are normal
- [ ] Application logs reviewed
- [ ] Event Viewer checked
- [ ] Database connectivity verified
- [ ] API/integration connectivity verified


## Monitoring Validation

- [ ] Monitoring status is healthy
- [ ] No critical alerts triggered
- [ ] Performance metrics are normal

---

# 8. Service Restart Specific Checklist

For application/service restart only:

- [ ] Identify affected service
- [ ] Verify service dependencies
- [ ] Stop service gracefully
- [ ] Start service successfully
- [ ] Confirm service status
- [ ] Validate application functionality

---

# 9. Restart Failure Handling

If restart does not resolve the issue:

- [ ] Capture current status
- [ ] Collect logs
- [ ] Check service failures
- [ ] Escalate to appropriate team
- [ ] Document actions performed

Avoid repeated restarts without analysis.

---

# 10. Restart Record Template

## Activity Details

| Field | Details |
|---|---|
| Application Name | |
| Server Name | |
| Environment | Production |
| Restart Date | |
| Performed By | |

## Reason for Restart

Reason:

## Validation Result

Result:

---

# 11. Best Practices

- Confirm impact before restarting production servers
- Avoid restarting during peak business hours
- Capture current health status before activity
- Validate application after restart
- Document restart reason and outcome
- Avoid restart as a permanent solution for recurring issues

---

**Document Purpose:** Production Server Restart Execution Checklist  
**Version:** 1.0
