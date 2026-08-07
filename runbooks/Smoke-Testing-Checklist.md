# Smoke Test Checklist

## 1. Purpose

This checklist provides a standard approach to validate critical application functionality after deployment, configuration changes, service restart, or environment activities.

The objective of smoke testing is to quickly confirm that the application is stable and ready for business usage.

---

# 2. Pre-Smoke Test Checks

Before starting smoke testing:

- [ ] Deployment activity is completed
- [ ] Application services are running
- [ ] Environment details are confirmed
- [ ] Required test access is available
- [ ] Database connectivity is verified
- [ ] Dependent services are available

---

# 3. Application Availability Checks

Verify basic application accessibility:

- [ ] Application URL is accessible
- [ ] Application page loads successfully
- [ ] No unexpected error message displayed
- [ ] Application response time is normal
- [ ] SSL certificate validation completed (if applicable)

---

# 4. Authentication Checks

Validate user authentication functionality:

- [ ] Login page is accessible
- [ ] Valid user login is successful
- [ ] Invalid login behaviour is verified
- [ ] User session is created successfully
- [ ] Logout functionality works correctly

---

# 5. Core Business Function Checks

Validate critical business workflows.

Examples:

- [ ] Create operation works
- [ ] Update operation works
- [ ] Search functionality works
- [ ] Data retrieval works
- [ ] Transaction processing works
- [ ] Reports/screens are loading correctly

Business scenarios should be selected based on application criticality.

---

# 6. Database Validation

Verify database-related functionality:

- [ ] Application connects successfully to database
- [ ] Data retrieval is working
- [ ] Data update operations are successful
- [ ] No database errors observed
- [ ] Required stored procedures/jobs are functioning

---

# 7. API and Integration Validation

Verify dependent integrations:

- [ ] Internal APIs are responding
- [ ] External APIs are reachable
- [ ] API authentication is successful
- [ ] Request and response flow is working
- [ ] Integration errors are not observed

---

# 8. Batch Job Validation

For applications using scheduled jobs:

- [ ] Scheduled jobs are running
- [ ] Previous jobs completed successfully
- [ ] No failed job execution observed
- [ ] Expected output/data generated

---

# 9. Log Validation

Review application and system logs:

Check for:

- [ ] Critical errors
- [ ] Application exceptions
- [ ] Authentication failures
- [ ] Database errors
- [ ] Integration failures

No critical errors should remain after successful deployment.

---

# 10. Monitoring Validation

Verify monitoring status:

- [ ] Application health checks are passing
- [ ] No critical alerts triggered
- [ ] Performance metrics are normal
- [ ] Server resources are within limits
- [ ] Monitoring dashboards show healthy status

---

# 11. Smoke Test Failure Handling

If smoke testing fails:

- [ ] Capture error details
- [ ] Collect relevant logs
- [ ] Inform deployment owner
- [ ] Assess business impact
- [ ] Decide rollback requirement
- [ ] Track issue through appropriate process

---

# 12. Smoke Test Completion

After successful validation:

- [ ] Test results documented
- [ ] Stakeholders informed
- [ ] Deployment status updated
- [ ] Application handed over for normal operations

---

# 13. Smoke Test Report Template

## Deployment Details

| Field | Details |
|---|---|
| Application Name | |
| Environment | |
| Deployment Version | |
| Deployment Date | |
| Tester | |


## Validation Results

| Test Area | Status | Comments |
|---|---|---|
| Application Access | | |
| Login | | |
| Business Functions | | |
| Database | | |
| API/Integration | | |
| Monitoring | | |

---

# 14. Best Practices

- Test critical functions first
- Use realistic business scenarios
- Record failures with evidence
- Avoid marking tests successful without validation
- Keep smoke test scenarios updated
- Automate repetitive checks where possible

---

**Document Purpose:** Production Smoke Testing Checklist  
**Version:** 1.0
