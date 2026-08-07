# Rollback Checklist

## 1. Purpose

This checklist provides a structured approach for rolling back application changes when a production deployment or configuration update causes unexpected issues.

The objective of rollback is to restore the last known stable application state safely and minimize business impact.

---

# 2. Rollback Initiation Criteria

Rollback should be considered when:

- [ ] Application is unavailable after deployment
- [ ] Critical business functionality is impacted
- [ ] Deployment introduces severe errors
- [ ] Application performance is significantly degraded
- [ ] Data processing is affected
- [ ] Critical integrations are failing

---

# 3. Pre-Rollback Assessment

Before starting rollback:

- [ ] Confirm rollback requirement
- [ ] Obtain required approval
- [ ] Inform stakeholders
- [ ] Identify rollback owner
- [ ] Confirm previous stable version availability
- [ ] Review rollback plan
- [ ] Assess business impact

---

# 4. Rollback Readiness Check

Verify availability of:

- [ ] Previous application package
- [ ] Previous configuration files
- [ ] Database rollback scripts (if applicable)
- [ ] Backup files
- [ ] Required access permissions
- [ ] Technical support availability

---

# 5. Communication Before Rollback

Notify relevant teams:

- [ ] Application support team
- [ ] Development team
- [ ] Infrastructure team
- [ ] Database team (if required)
- [ ] Business stakeholders

Communication should include:

- Reason for rollback
- Expected impact
- Rollback start time
- Expected recovery timeline

---

# 6. Rollback Execution Checklist

## Application Rollback

- [ ] Stop required application components
- [ ] Remove failed deployment version
- [ ] Restore previous application version
- [ ] Restore previous configuration
- [ ] Start application components


## Database Rollback (If Required)

- [ ] Confirm database rollback requirement
- [ ] Validate rollback script
- [ ] Execute approved rollback steps
- [ ] Verify database consistency


## Service Validation

- [ ] Required services are running
- [ ] Application pools are healthy
- [ ] Background processes are functioning

---

# 7. Post-Rollback Validation

## Application Validation

- [ ] Application is accessible
- [ ] User login is working
- [ ] Critical business functions are validated
- [ ] Application response is normal


## Technical Validation

- [ ] Application logs reviewed
- [ ] Database connectivity verified
- [ ] API/integration connectivity checked
- [ ] Monitoring status verified
- [ ] No critical errors observed

---

# 8. Rollback Completion

After successful rollback:

- [ ] Confirm application stability
- [ ] Inform stakeholders
- [ ] Update change record
- [ ] Record rollback details
- [ ] Capture deployment failure details
- [ ] Plan next corrective action

---

# 9. Rollback Failure Handling

If rollback fails:

- [ ] Stop further changes
- [ ] Assess current application state
- [ ] Escalate to required teams
- [ ] Restore service using alternate recovery approach
- [ ] Document actions performed

---

# 10. Rollback Record Template

## Change Details

| Field | Details |
|---|---|
| Application Name | |
| Environment | Production |
| Deployment Version | |
| Rollback Version | |
| Rollback Date | |
| Performed By | |

## Rollback Reason

Reason:

## Rollback Outcome

Result:

---

# 11. Rollback Best Practices

- Always maintain a tested rollback plan
- Do not start rollback without understanding impact
- Preserve deployment failure evidence
- Validate application after rollback
- Document actual rollback steps performed
- Review failed deployments for improvements

---

**Document Purpose:** Production Rollback Execution Checklist  
**Version:** 1.0
