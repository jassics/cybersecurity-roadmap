# Web Security Skills and Career Roadmap
Web Security is the most common **entry point** into cybersecurity. If you can read code, understand HTTP, and exploit the OWASP Top 10, you can start almost anywhere in AppSec, Pentesting, or DevSecOps.

## Who is this for?
- Computer Science / IT graduates curious about ethical hacking
- Developers / QA who want to pivot into security
- Bug bounty enthusiasts wanting a full-time security job

## Pre-requisites (foundation)
Before jumping into web security, get comfortable with:

1. HTTP/HTTPS request-response lifecycle, headers, status codes, cookies, sessions
2. HTML, CSS, JavaScript basics (you must be able to read JS)
3. One backend language — Python, Node.js, PHP, Java, or Go
4. SQL basics (queries, joins) — required to understand SQLi
5. Linux commands (see [common-skills.md](common-skills.md))
6. Git basics
7. Basic networking (DNS, TCP/IP, TLS handshake)

## Career ladder

### Entry level (0–2 years)
**Possible job titles:**

- Security Intern / Trainee
- Application Security Analyst
- VAPT Analyst (Web)
- Junior Penetration Tester
- Bug Bounty Hunter (independent)

**Skills to focus on:**

1. **OWASP Top 10** — SQLi, XSS, CSRF, SSRF, IDOR, Broken Auth, XXE, Insecure Deserialization, etc.
2. **Burp Suite Community** — proxying, repeater, intruder, decoder
3. **Manual testing** — be able to find a bug without a scanner
4. **Recon basics** — subdomain enumeration, content discovery (ffuf, dirsearch, subfinder, amass)
5. **Browser DevTools** — network tab, console, storage inspection
6. **Common scanners (light touch)** — Nikto, OWASP ZAP, Nuclei
7. Reading and writing simple **PoC scripts** in Python
8. Writing clear **vulnerability reports** (Title, Severity, Steps to Reproduce, Impact, Fix)

**Practice platforms:**

- PortSwigger Web Security Academy (free, gold standard)
- HackTheBox, TryHackMe
- DVWA, Juice Shop, WebGoat
- HackerOne, Bugcrowd public programs

**Entry-level certs (optional but help in resumes):**

- eJPT, CompTIA Security+, CEH (only if your region demands it)

### Mid level (2–5 years)
**Possible job titles:**

- Application Security Engineer
- Web Penetration Tester
- Security Consultant
- Bug Bounty Hunter (full-time)

**New skills to add:**

1. **OWASP API Top 10** — BOLA, mass assignment, etc. (see [api-security.md](api-security.md))
2. **Authentication deep dive** — OAuth2.0, OIDC, SAML, JWT pitfalls
3. **Modern web stack threats** — GraphQL, WebSockets, SSE, gRPC over HTTP
4. **Single Page Apps & framework-specific issues** — React XSS sinks, Angular sanitization, prototype pollution
5. **SSRF chained with cloud metadata** (169.254.169.254 IMDSv1)
6. **Source code review** — SAST tooling, secure code review for at least one language
7. **CI/CD integration** — running DAST/SAST in pipelines
8. **Bypass techniques** — WAF bypass, filter bypass, encoding tricks
9. Burp Suite **Professional** — extensions, macros, Bambdas
10. Writing **custom Burp extensions** or Nuclei templates

**Certs to consider:**

- OSCP (network + web mix)
- OSWE (web expert, code review heavy)
- eWPTXv2
- Burp Suite Certified Practitioner

### Senior level (5–8 years)
**Possible job titles:**

- Senior Application Security Engineer
- Lead Penetration Tester
- Product Security Engineer
- Senior Security Consultant

**New responsibilities & skills:**

1. **Threat modeling** — STRIDE, attack trees, PASTA
2. **Secure SDLC** — embed security into design reviews, sprint planning
3. **Mentoring** L1/L2 testers, reviewing reports
4. **Vendor selection** for SAST/DAST/IAST/RASP tools
5. **Security champions program** in engineering
6. **Cross-domain depth** — at least one of: cloud, mobile, API, infra pentest
7. **Communication with engineering and product** leadership

### Staff / Principal / Architect (8+ years)
**Possible job titles:**

- Staff Application Security Engineer
- Principal Product Security Engineer
- Application / Product Security Architect
- Head of AppSec

**Focus areas:**

- Security strategy across the org
- Building paved-road / secure-by-default libraries
- Org-wide threat modeling, risk acceptance frameworks
- Security architecture reviews, RFC reviews
- Vendor + tool consolidation, cost optimization
- Hiring + team building

## Career paths from Web Security

```text
                       Web Security (entry)
                              │
       ┌──────────────┬───────┴───────┬──────────────┐
       ▼              ▼               ▼              ▼
  Application      API Security    Penetration    Bug Bounty
  Security                          Testing       (independent)
       │              │               │              │
       ▼              ▼               ▼              ▼
  Product Sec   API Architect    Red Team /     Security
  Engineer                       Adversary      Researcher
       │                         Emulation
       ▼
  DevSecOps  ───────►  Cloud Security  ───►  Security Architect
```

## Lateral pivots specifically from Web Security
- **→ API Security** — natural next step; most apps are APIs today
- **→ Mobile Security** — same OWASP-style mindset, different platform
- **→ Cloud Security** — once you understand SSRF/IAM, cloud opens up
- **→ DevSecOps** — automate the testing you do manually
- **→ Red Team** — chain web bugs into full network compromise
- **→ Security Research** — find 0-days in popular CMS / frameworks

## AI-augmented Web Security (you need this in 2025+)
AI is changing both **how you do web security** and **what you need to secure**. Add these skills on top of everything above:

### Using AI to do web security better
1. **AI-assisted recon and exploitation** — Burp Suite's AI features, ShellGPT, PentestGPT-style assistants; know how to prompt for payload variants and bypass ideas
2. **AI for code review** — use GitHub Copilot Chat, Cursor, Claude Code to read unfamiliar codebases 10x faster; cross-check with Semgrep / CodeQL
3. **AI for report writing** — get first drafts of vulnerability descriptions, impact statements, and remediation guidance (always review for accuracy)
4. **Custom GPTs / agents** for repetitive recon, payload triage, and OSINT
5. **Beware of LLM hallucination** — AI will confidently invent CVE numbers and library functions. Verify everything.

### Securing AI features inside web apps
Modern web apps embed chatbots, RAG, copilots, and agents. As a web security person you'll need:

1. **OWASP Top 10 for LLM Applications** — prompt injection (direct + indirect), insecure output handling, sensitive info disclosure, excessive agency, etc.
2. **Prompt injection in web context** — `<img src=x>` style injections that exfiltrate via markdown/HTML, indirect injection via fetched docs
3. **Output handling** — treat LLM output as **untrusted user input**; sanitize before rendering, before SQL, before shell
4. **Server-side request forgery via AI tools** — agents fetching URLs become a new SSRF vector
5. **Data exfiltration via markdown rendering** — image / link tags built from LLM output leaking conversation state
6. **Rate limiting + cost controls** — LLM endpoints are expensive; abuse = financial DoS
7. **Authentication & authorization for AI features** — does the agent enforce the user's permissions, or its own service account?

See: [AI Security Career Roadmap](ai-security-career-roadmap.md) and [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

## Recommended books
- *The Web Application Hacker's Handbook 2* — Stuttard & Pinto
- *Real-World Bug Hunting* — Peter Yaworski
- *Bug Bounty Bootcamp* — Vickie Li
- *Alice and Bob Learn Application Security* — Tanya Janca

## Recommended creators / blogs
- PortSwigger research blog
- HackerOne Hacktivity
- @nahamsec, @InsiderPhD, @stokfredrik on YouTube

> 📘 Recommended study plans: [Secure Code Review](https://github.com/jassics/security-study-plan/blob/main/secure-code-review-study-plan.md) · [Product Security](https://github.com/jassics/security-study-plan/blob/main/product-security-study-plan.md) · [Common Skills](https://github.com/jassics/security-study-plan/blob/main/common-skills-study-plan.md). Tick them off as you go.

## Next step
Open [api-security.md](api-security.md), [common-skills.md](common-skills.md), and pick **one practice platform** to grind 4–6 hours per week. Consistency beats intensity in this domain.
