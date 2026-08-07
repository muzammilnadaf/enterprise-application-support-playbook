# Deployment Checklist

## 1. Purpose

This checklist provides a standard approach for executing application deployments safely in production environments.

The objective is to ensure deployment readiness, minimize risks, and complete required validations after deployment.

---

# 2. Pre-Deployment Checklist

## Change and Approval Validation

- [ ] Change request is approved
- [ ] Deployment window is confirmed
- [ ] Required stakeholders are informed
- [ ] Deployment owner is assigned
- [ ] Support team availability is confirmed


## Deployment Package Validation

- [ ] Correct build/version is identified
- [ ] Deployment package is available
- [ ] Package integrity is verified
- [ ] Deployment instructions are reviewed
- [ ] Database scripts are reviewed (if applicable)


## Environment Validation

- [ ] Target environment is confirmed
- [ ] Application servers are reachable
- [ ] Required access is available
- [ ] Disk space is checked
- [ ] Current application health is verified


## Backup and Recovery Readiness

- [ ] Application backup completed (if required)
- [ ] Database backup completed (if required)
- [ ] Rollback plan is available
- [ ] Previous stable version is identified


## Dependency Validation

Verify dependent components:

- [ ] Database availability
- [ ] External APIs availability
- [ ] Integration services status
- [ ] File locations/access
- [ ] Required services running

---

# 3. Deployment Execution Checklist

## Before Deployment

- [ ] Notify stakeholders about deployment start
- [ ] Capture current application status
- [ ] Stop required services (if applicable)
- [ ] Take required configuration backup
- [ ] Confirm deployment steps


## During Deployment

- [ ] Follow approved deployment steps
- [ ] Deploy application components
- [ ] Apply database changes (if applicable)
- [ ] Update configuration changes
- [ ] Monitor deployment progress
- [ ] Capture deployment issues or observations


## Deployment Verification

- [ ] Deployment completed successfully
- [ ] No unexpected errors observed
- [ ] Application services are running
- [ ] Application is accessible
- [ ] Logs are reviewed

---

# 4. Post-Deployment Validation

## Application Validation

- [ ] Application URL is accessible
- [ ] User login functionality is verified
- [ ] Critical business flow is tested
- [ ] Application response is normal


## Technical Validation

- [ ] Application logs checked
- [ ] Server logs checked
- [ ] Database connectivity verified
- [ ] API/integration connectivity verified
- [ ] Monitoring dashboards checked


## Business Validation

- [ ] Business users notified
- [ ] Business validation completed (if required)
- [ ] No critical issues reported

---

# 5. Deployment Completion Checklist

- [ ] Deployment status communicated
- [ ] Change ticket updated
- [ ] Deployment evidence attached
- [ ] Issues encountered documented
- [ ] Support documentation updated (if required)
- [ ] Deployment completed successfully

---

# 6. Deployment Failure Checklist

If deployment fails:

- [ ] Stop further deployment activities
- [ ] Assess application impact
- [ ] Inform stakeholders
- [ ] Review deployment logs
- [ ] Decide rollback requirement
- [ ] Execute rollback procedure if approved
- [ ] Validate application recovery
- [ ] Document failure details


---

# 7. Common Deployment Validation Points

| Area | Validation |
|---|---|
| Application | Application loads successfully |
| Services | Required services are running |
| Database | Connectivity and scripts completed successfully |
| APIs | External/internal communication working |
| Logs | No critical errors observed |
| Monitoring | No active critical alerts |

---

# 8. Deployment Best Practices

- Always validate the correct build before deployment
- Do not skip rollback preparation
- Avoid manual changes without documentation
- Monitor application behaviour after deployment
- Communicate status clearly
- Document actual activities performed

---

**Document Purpose:** Production Deployment Execution Checklist  
**Version:** 1.0
