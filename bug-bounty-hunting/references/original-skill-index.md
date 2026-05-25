# Original Claude-BugHunter Skill Index

This file documents the full 51-skill index from the original [elementalsouls/Claude-BugHunter](https://github.com/elementalsouls/Claude-BugHunter) repository. Skills marked with ✅ have been adapted for Hermes. Skills marked with ⬜ have not yet been adapted.

## Adapted Skills (10 hunt + 4 support = 14 total)

✅ **bug-bounty-hunting** — Master orchestrator (5-phase workflow, A→B chains)  
✅ **hunt-xss** — Cross-Site Scripting (174 H1 report patterns)  
✅ **hunt-ssrf** — Server-Side Request Forgery (cloud metadata, IP bypass)  
✅ **hunt-sqli** — SQL Injection + NoSQL Injection (MySQL, PG, MSSQL, Oracle, MongoDB)  
✅ **hunt-rce** — Remote Code Execution (SSTI, deserialization, dependency confusion)  
✅ **hunt-idor** — Insecure Direct Object References (10+ patterns, cross-tenant)  
✅ **hunt-ato** — Account Takeover (9 ATO paths)  
✅ **hunt-auth-bypass** — Authentication Bypass (12 bypass classes)  
✅ **hunt-api-misconfig** — API misconfiguration (JWT, GraphQL, CORS, mass assignment)  
✅ **hunt-file-upload** — File Upload (10 exploitation techniques)  
✅ **triage-validation** — 7-Question Gate, never-submit list, CVSS scoring  
✅ **security-arsenal** — Complete payload library (all vuln classes)  
✅ **report-writing** — Report templates (H1, Bugcrowd, Intigriti, Immunefi)  
✅ **redteam-mindset** — Red team discipline, engagement cadence

## Not Yet Adapted

### Web Application Vulnerabilities (8 missing)

⬜ **hunt-ssti** — Server-Side Template Injection  
⬜ **hunt-xxe** — XML External Entity attacks  
⬜ **hunt-csrf** — Cross-Site Request Forgery (chain-required impact)  
⬜ **hunt-business-logic** — Business Logic Flaws  
⬜ **hunt-cache-poison** — Web Cache Poisoning  
⬜ **hunt-http-smuggling** — HTTP Request Smuggling  
⬜ **hunt-race-condition** — Race Conditions  
⬜ **hunt-llm-ai** — LLM/AI Security Testing

### Authentication & Identity (3 missing)

⬜ **hunt-mfa-bypass** — MFA/2FA Bypass (7 patterns)  
⬜ **hunt-oauth** — OAuth 2.0/OIDC flaws (10 H1 reports)  
⬜ **hunt-saml** — SAML SSO attacks

### API & Infrastructure (4 missing)

⬜ **hunt-graphql** — GraphQL API attacks  
⬜ **hunt-cloud-misconfig** — Cloud misconfiguration (S3, Lambda, kubelet)  
⬜ **hunt-subdomain** — Subdomain enumeration  
⬜ **hunt-ntlm-info** — NTLM information disclosure

### Enterprise Platform Attacks (7 missing)

⬜ **m365-entra-attack** — Microsoft 365/Entra ID attacks  
⬜ **okta-attack** — Okta identity platform attacks  
⬜ **cloud-iam-deep** — Cloud IAM deep dive  
⬜ **vmware-vcenter-attack** — VMware vCenter attacks  
⬜ **enterprise-vpn-attack** — Enterprise VPN attack vectors  
⬜ **hunt-sharepoint** — SharePoint vulnerabilities  
⬜ **hunt-aspnet** — ASP.NET specific vulnerabilities

### Operations & Reporting (6 missing)

⬜ **bug-bounty** — General bug bounty skills  
⬜ **bb-methodology** — Bug bounty methodology (subsumed into orchestrator)  
⬜ **bugcrowd-reporting** — Bugcrowd-specific reporting  
⬜ **evidence-hygiene** — PoC capture, cookie redaction, PII masking, HAR sanitization  
⬜ **mid-engagement-ir-detection** — Mid-engagement IR detection  
⬜ **offensive-osint** — Offensive OSINT techniques  
⬜ **osint-methodology** — OSINT methodology

### Specialized Domains (5 missing)

⬜ **web3-audit** — Web3/blockchain auditing  
⬜ **meme-coin-audit** — Meme coin security audit  
⬜ **supply-chain-attack-recon** — Supply chain attack reconnaissance  
⬜ **apk-redteam-pipeline** — Android APK red team pipeline  
⬜ **web2-recon** — Web 2.0 reconnaissance

### Dispatching & Local Toolkit (2 missing)

⬜ **hunt-dispatch** — Hunting dispatch/coordination  
⬜ **bb-local-toolkit** — Bug bounty local toolkit

---

## How to Adapt a Skill

1. Load the original content: `https://raw.githubusercontent.com/elementalsouls/Claude-BugHunter/main/skills/{name}/SKILL.md`
2. Wrap in Hermes YAML frontmatter:
```yaml
---
name: {name}
description: |
  {one-paragraph description}
triggers:
  - trigger phrase 1
  - trigger phrase 2
category: security
---
```
3. Place at `~/.hermes/skills/bug-bounty/{name}/SKILL.md`
4. Verify with `skill_view(name='{name}')`
5. Add a reference in `references/original-skill-index.md` changing ⬜ to ✅
