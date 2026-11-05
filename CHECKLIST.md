# Secure Development Checklist

Name: PEREZ
Date: 5 November 2026

## 1. Pipeline map

| Stage | Security activity | Example tool | Gate (what blocks progress) |
| --- | --- | --- | --- |
| Plan | Write security requirements and assess risk | Checklist, gap analysis | Requirements approved |
| Design | Threat modelling | STRIDE | Top threats have countermeasures |
| Code | Scan while you type and peer review | SonarQube for IDE, Snyk IDE plugin | No hard-coded secrets, pull request reviewed |
| Build | SAST, SCA and secrets scan | Snyk, Dependency-Check | No new High or Critical findings |
| Test | Security tests and DAST | OWASP ZAP, penetration test | No open High findings |
| Deploy | Harden configuration and protect secrets | Security headers, secrets manager | Configuration checklist signed off |
| Operate | Monitor, patch and audit | Dependabot, logs, scheduled scans | Critical patches within agreed time |

## 2. My own additions (one more security activity for each stage)

- Plan: Identify sensitive data and classify it according to its importance.
- Design: Review the system architecture to identify weak points before development begins.
- Code: Validate user input to prevent injection attacks.
- Build: Check third-party libraries for known vulnerabilities before packaging the application.
- Test: Test user permissions to ensure users cannot access information they are not authorised to see.
- Deploy: Enable multi-factor authentication (MFA) for administrative accounts.
- Operate: Review access logs regularly to identify unusual login attempts or suspicious activities.

## 3. My pass or fail rules for three gates

1. Gate: Build. Rule: the build fails if Snyk reports any High or Critical issue.
2. Gate:
3. Gate:

## 4. SonarQube for IDE warnings I saw in app.js

Improper input validation exposed sensitive data/information from the database to an anauthorized user/client/agent

Solution: Proper input validation (by design) to prevent aunauthorized data exposure.
## 5. Snyk for IDE Warnings I saw in app.js
