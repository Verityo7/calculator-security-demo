## DAST WARN-NEW Findings

| Code | Issue | RIsk | Affected URL           | Why It Matters        |
|------|------------|------------|------------------------|----------------------------------|
| 10020 | Missing Anti-clickjacking Header    | Medium    | http://localhost:5000  | Clickjacking attacks possible  |
| 10021 | X-Content-Type-Options Header Missing     | Low     | http://localhost:5000  | MIME-sniffing attacks possible |
| 10036 | Server Leaks Version Information via "Server" HTTP Response Header Field   | Low     | http://localhost:5000  http://localhost:5000/robots.txt http://localhost:5000/sitemap.xml | Information disclosure |
| 10038 | Content Security Policy (CSP) Header Not Set     | Medium     | http://localhost:5000  http://localhost:5000/robots.txt | XSS and injection attacks possible |
| 10063 | Permissions Policy Header Not Set  | Low     | http://localhost:5000  http://localhost:5000/robots.txt http://localhost:5000/sitemap.xml | Malicious scripts could access browser features |
| 90004 | Insufficient Site Isolation Against Spectre Vulnerability  | Low     | http://localhost:5000 | Side-channel information leak |

