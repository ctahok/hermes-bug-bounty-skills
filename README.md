# Hermes Bug Bounty Hunting Skills

Bug bounty hunting skills adapted from [Claude-BugHunter](https://github.com/elementalsouls/Claude-BugHunter) by ElementalSouls (Sachin Sharma) for [Hermes Agent](https://github.com/NousResearch/hermes-agent).

14 skills covering the complete bug hunting lifecycle: methodology, reconnaissance, active exploitation, triage, and reporting.

## Skills

| Skill | Lines | Coverage |
|---|---|---|
| **bug-bounty-hunting** | 348 | Master orchestrator — 5-phase workflow, crown jewel targeting, A→B chain matrix |
| **triage-validation** | 209 | 7-Question Gate, never-submit list, 4 pre-submission gates, CVSS scoring |
| **security-arsenal** | 506 | Complete payload library — XSS, SSRF, SQLi, XXE, SSTI, JWT, path traversal, command injection |
| **hunt-xss** | 566 | Reflected/stored/DOM/blind XSS. 174 H1 pattern library, CSP bypasses, mXSS |
| **hunt-ssrf** | 264 | Cloud metadata (AWS/GCP/Azure), IP bypass, OOB confirmation gate |
| **hunt-idor** | 281 | 10+ IDOR patterns, horizontal/vertical escalation, UUID enumeration, cross-tenant |
| **hunt-sqli** | 789 | Classic/blind/time-based SQLi for MySQL/PG/MSSQL, NoSQLi, WAF bypasses |
| **hunt-rce** | 266 | SSTI (Jinja2/Twig/Freemarker/Velocity), command injection, deserialization |
| **hunt-ato** | 206 | 9 ATO paths — credential stuffing, reset poisoning, OAuth linkage, session hijacking |
| **hunt-auth-bypass** | 201 | 12 bypass classes — method tampering, API downgrade, default creds, header injection |
| **hunt-api-misconfig** | 240 | JWT attacks, GraphQL introspection + batching, CORS, prototype pollution |
| **hunt-file-upload** | 184 | 10 upload techniques — double ext, magic bytes, ZIP slip, SVG XSS, polyglot |
| **report-writing** | 249 | H1/Bugcrowd/Intigriti/Immunefi templates, CVSS 3.1, evidence hygiene |
| **redteam-mindset** | 137 | Red team discipline, anti-patterns, engagement cadence |

## Installation

```bash
# Clone the repo
git clone https://github.com/ctahok/hermes-bug-bounty-skills.git

# Copy skills to Hermes
cp -r hermes-bug-bounty-skills/* ~/.hermes/skills/bug-bounty/
```

Skills auto-load when you use matching trigger phrases like "hunt XSS", "test for SQL injection", "hunt this target for bugs".

## Credits

Original work: [Claude-BugHunter](https://github.com/elementalsouls/Claude-BugHunter) by **Sachin Sharma** (ElementalSouls) — 51 skills, 15 slash commands, 574+ disclosed HackerOne report patterns across 24 vulnerability classes.

Adapted for Hermes Agent by Hermes Agent.
