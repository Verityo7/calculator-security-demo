# Scanner Comparison

## Only CodeQL (SAST) Found
- No code vulnerabilities detected in this run.
- One pipeline warning: CodeQL Action v3 will be deprecated in December 2026 → update to v4.
- SAST focuses on code-level issues (e.g., SQL injection in source, hardcoded secrets, insecure data flow) that DAST cannot see because it only tests the running app.

## Only ZAP (DAST) Found
- Content Security Policy (CSP) Header Not Set (Issue Code 10038, Medium risk).
- Missing Anti-clickjacking Header (Issue Code 10020, Medium risk).
- Insufficient Site Isolation Against Spectre Vulnerability (Issue Code 90004, Low risk)
- Permissions Policy Header Not Set (Issue Code 10063, Low risk).
- Server Leaks Version Information via "Server" HTTP Response Header Field (Issue Code 10036, Low risk).
- X-Content-Type-Options Header Missing (Issue Code 10021, Low risk).
- Informational findings: Modern Web Application, Sec-Fetch headers missing, Storable and Cacheable Content
- These runtime configuration issues are only visible when the app is running, so SAST and SCA cannot detect them.

## Only Dependency-Check (SCA) Found
- No vulnerable dependencies detected in this run.
- SCA uniquely identifies outdated or insecure third-party packages (e.g., Flask, Werkzeug) when present. In this case, all dependencies scanned clean.

## All Three Tools
- No overlapping findings in this run.
