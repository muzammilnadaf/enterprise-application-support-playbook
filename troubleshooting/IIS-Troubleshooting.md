# IIS Troubleshooting Guide

## 1. Overview

Internet Information Services (IIS) is a web server platform commonly used to host enterprise applications, especially .NET-based applications.

IIS issues can impact application availability, performance, authentication, and request processing.

Common IIS problems include:

- Website not accessible
- Application Pool failures
- HTTP errors
- Configuration issues
- SSL certificate problems
- Slow response
- Application crashes

---

# 2. IIS Troubleshooting Approach

Follow a structured approach:


Understand Issue
<br>&#11015;<br>
Check IIS Availability
<br>&#11015;<br>
Validate Website/Application Pool
<br>&#11015;<br>
Review Logs
<br>&#11015;<br>
Check Configuration
<br>&#11015;<br>
Identify Root Cause
<br>&#11015;<br>
Apply Fix
<br>&#11015;<br>
Validate Application


---

# 3. Initial Information Collection

Before troubleshooting, collect:

- Application URL
- Affected environment
- Error message
- HTTP status code
- Issue start time
- Recent deployments or changes
- Affected users
- Server details


Important questions:

- Is the website completely unavailable?
- Are all users affected?
- Did the issue start after a deployment?
- Is the issue application-specific or server-wide?

---

# 4. IIS Service Validation

Check IIS services:

## World Wide Web Publishing Service (W3SVC)

Verify:

- Service status is running
- Service startup type is correct
- No service failures reported


Actions:

- Check Windows Services
- Review Event Viewer logs
- Restart service only after analysis

---

# 5. Website Availability Troubleshooting

Common symptoms:

- Website not loading
- Connection refused
- HTTP errors


Checks:

- IIS website status
- Binding configuration
- Application Pool status
- Server connectivity
- Firewall/network access


Validate:

- Website is started
- Correct port is configured
- Correct hostname is mapped

---

# 6. Application Pool Troubleshooting

Application Pools isolate applications and manage worker processes.

## Common Issues

- Application Pool stopped
- Frequent recycling
- Worker process crashes
- Memory limit exceeded


## Checks

Verify:

- Application Pool status
- .NET CLR version
- Identity configuration
- Recycling settings
- Memory usage


## Common Causes

- Application exceptions
- Memory leaks
- Incorrect configuration
- Permission issues


Actions:

- Review logs
- Check Event Viewer
- Analyse application errors
- Restart only when required

---

# 7. Worker Process Troubleshooting

The IIS worker process (w3wp.exe) handles application requests.

Common symptoms:

- Slow application response
- Application unavailable
- High CPU usage


Checks:

- w3wp.exe CPU usage
- Memory consumption
- Multiple worker processes
- Application logs


Possible causes:

- Code issues
- Long-running requests
- Database delays
- Memory leaks

---

# 8. HTTP Error Troubleshooting

## HTTP 400 - Bad Request

Possible causes:

- Invalid request
- Incorrect headers
- Large request size


Checks:

- Request details
- Application configuration
- Client request data


---

## HTTP 401 - Unauthorized

Possible causes:

- Authentication failure
- Incorrect credentials
- Authentication configuration issue


Checks:

- IIS authentication settings
- User permissions
- Application security configuration


---

## HTTP 403 - Forbidden

Possible causes:

- Access restrictions
- Missing permissions
- Directory browsing disabled


Checks:

- IIS authorization rules
- Folder permissions
- Authentication settings


---

## HTTP 404 - Not Found

Possible causes:

- Incorrect URL
- Missing application path
- Deployment issue


Checks:

- IIS application mapping
- Physical path
- Deployment files


---

## HTTP 500 - Internal Server Error

Possible causes:

- Application exception
- Configuration error
- Runtime failure


Checks:

- Application logs
- web.config
- Windows Event Viewer
- IIS logs


---

# 9. web.config Troubleshooting

Configuration issues are common after deployments.

Check:

- Syntax errors
- Connection strings
- Application settings
- Authentication settings
- Runtime configuration


Common symptoms:

- Application startup failure
- HTTP 500 errors
- Configuration errors


Best practice:

- Compare with previous working configuration
- Validate changes before deployment

---

# 10. SSL Certificate Troubleshooting

Common symptoms:

- HTTPS not working
- Certificate warnings
- Secure connection failures


Checks:

- Certificate validity
- Expiry date
- Binding configuration
- Certificate chain
- Correct hostname mapping


Resolution:

- Renew certificate if expired
- Update IIS binding
- Validate HTTPS access

---

# 11. IIS Logs Analysis

IIS logs provide request-level information.

Default location:


C:\inetpub\logs\LogFiles



Review:

- Request URL
- Status code
- Sub-status code
- Response time
- Client information


Examples:


500.19 - Configuration issue

503 - Service unavailable


---

# 12. Windows Event Viewer Analysis

Check:


Event Viewer
|
Windows Logs
|
Application/System



Look for:

- Application crashes
- .NET runtime errors
- Service failures
- Configuration issues


Important details:

- Error timestamp
- Exception message
- Application name
- Faulting module

---

# 13. IIS Performance Troubleshooting

Common symptoms:

- Slow page response
- High CPU
- High memory usage


Checks:

## Server Level

- CPU usage
- Memory utilization
- Disk availability


## IIS Level

- Active requests
- Worker process usage
- Application Pool health


## Application Level

- Database response
- External API response
- Application exceptions

---

# 14. Common IIS Recovery Actions

Possible actions:

- Restart application pool
- Restart IIS service
- Clear temporary files (if approved)
- Restore configuration
- Roll back recent changes


Always:

- Understand impact
- Capture evidence
- Validate after action

---

# 15. IIS Troubleshooting Checklist

- [ ] Confirm application URL issue
- [ ] Check IIS service status
- [ ] Verify website status
- [ ] Verify Application Pool status
- [ ] Check worker process health
- [ ] Review IIS logs
- [ ] Review Event Viewer
- [ ] Validate configuration
- [ ] Check SSL certificate
- [ ] Confirm application recovery

---

# 16. Best Practices

- Avoid restarting IIS without investigation
- Review logs before applying fixes
- Maintain IIS configuration backups
- Document configuration changes
- Monitor Application Pool behaviour
- Validate application after recovery

---

# 17. Summary

Effective IIS troubleshooting requires understanding the relationship between IIS configuration, application behaviour, server resources, and dependencies.

A structured approach helps support teams:

- Restore application availability quickly
- Reduce unnecessary restarts
- Identify configuration issues
- Improve production stability

---

**Document Purpose:** IIS Troubleshooting Guide  
**Version:** 1.0
