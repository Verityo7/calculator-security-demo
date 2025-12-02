# Security Scanning

## Overview
This repository uses three types of security scanning:

### SAST (Static Analysis with CodeQL)
- Scans source code for vulnerabilities
- Runs on push to main branch
- Checks for: 
    - Code injection vulnerabilities
    - Hardcoded secrets and sensitive data
    - Insecure configurations
    - Insecure data flow patterns
    - OWASP Top 10 vulnerabilities
- Artifacts: See GitHub Security tab
- Workflow: [.github/workflows/1-sast-only.yml](.github/workflows/1-sast-only.yml)

### SCA (Dependency Check)
- Scans Python packages for known CVEs
- Runs on push to main branch
- Checks for: 
    - Outdated dependencies with CVEs
    - Known vulnerable packages
    - License compliance issues
- Artifacts: sca-reports
- Workflow: [.github/workflows/2-sca-only.yml](.github/workflows/2-sca-only.yml)

### DAST (Live Application with ZAP)
- Tests running application for vulnerabilities
- Runs on push to main branch
- Checks for: 
    - SQL injection
    - Cross-site scripting (XSS)
    - Security misconfigurations
    - Broken authentication
- Artifacts: zap-baseline-reports, zap-baseline-scan, zap-fullscan-reports, zap-fullscan-scan
- Workflow: [.github/workflows/3-dast-only.yml](.github/workflows/3-dast-only.yml)

## Understanding Results
- **PASS:** No issues detected
- **WARN-NEW:** New warnings requiring review
- **WARN-INPROG:** Warnings previously identified are still present
- **FAIL-NEW:** Critical issues requiring immediate fixes
- **FAIL-INPROG:** Critical issues previously identified are still present
- **INFO:** Informational findings which do not require action, lower priority

## Reporting Vulnerabilities
Please email security@example.com