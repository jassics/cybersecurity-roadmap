# Software Security Skills and Career Roadmap

> 📘 Recommended study plans: [Secure Code Review](https://github.com/jassics/security-study-plan/blob/main/secure-code-review-study-plan.md) · [Secure Software Development Lifecycle](https://github.com/jassics/security-study-plan/blob/main/secure-software-development-lifecycle-study-plan.md) · [Product Security](https://github.com/jassics/security-study-plan/blob/main/product-security-study-plan.md).

Software Security is **code-level** security — the deepest end of the AppSec spectrum. This is where you read source code, do threat modeling, build secure libraries, fix systemic vulnerability classes, and influence the SDLC. It overlaps heavily with Application Security but tilts more toward **engineering and design** than testing.

## Software Security vs. Application Security
| Aspect | Software Security | Application Security |
|--------|------------------|----------------------|
| Focus | Building software securely | Testing & fixing apps |
| Primary work | Code review, threat models, secure design, libraries | Pentesting, scanners, triage |
| Output | Secure code, design docs, frameworks | Bug reports, mitigation guidance |
| Day-to-day | Closer to a developer | Closer to a pentester |

In practice, many companies use the titles interchangeably. The track described here is the **deep-engineering side**.

## Who is this for?
- Developers who want to specialize in security
- AppSec engineers tired of pentest-only work, wanting deeper design influence
- Folks who love reading code more than running scanners

## Pre-requisites
1. **Strong programming** in at least one production language — C/C++, Java, C#, Go, Rust, Python, or JavaScript/TypeScript
2. **Data structures, OS concepts, memory model** (stack vs heap, pointers, GC basics)
3. **OWASP Top 10** and **OWASP ASVS** working knowledge
4. **Git** and code review etiquette
5. **Threat modeling fundamentals** (STRIDE)
6. **Build systems** — Maven/Gradle/npm/Cargo/Go modules

## Career ladder

### Entry level (0–2 years)
**Possible job titles:**

- Junior Software Security Engineer
- Secure Code Reviewer (Junior)
- Application Security Engineer (code review-leaning)

**Skills to focus on:**

1. **Manual secure code review** for one language — find SQLi, XSS, IDOR, deserialization, command injection from code
2. **Common vulnerability sinks** — `eval`, `exec`, `Runtime.exec`, `system`, raw SQL concat, `innerHTML`, `pickle.loads`
3. **SAST tooling** — Semgrep, CodeQL, SonarQube; writing your first custom rule
4. **Cryptography essentials** — hashing vs encryption, salting, KDFs (bcrypt/argon2/scrypt), symmetric vs asymmetric, common misuses
5. **OWASP Cheat Sheet Series** — read your top 5 cheat sheets cold
6. **Secure coding standards** — CERT, OWASP Proactive Controls
7. **Reading CVEs** — pick one CVE per week, understand the root cause from the patch

### Mid level (2–5 years)
**Possible job titles:**

- Software Security Engineer
- Product Security Engineer (Software)
- Secure Code Review Lead

**New skills to add:**

1. **Multi-language code review** — at least one strongly-typed (Java/Go/C#) and one dynamic (Python/Node)
2. **Custom SAST rule development** — CodeQL queries, Semgrep rules for org-specific patterns
3. **Memory safety** (if in C/C++/Rust ecosystem) — buffer overflows, UAF, double-free, race conditions; mitigations (ASLR, DEP, CFI, StackGuard)
4. **Threat modeling at scale** — STRIDE, attack trees, PASTA, lightweight design reviews
5. **Secure-by-default libraries** — wrapping crypto, HTTP clients, auth flows for internal use
6. **Bug class elimination** — eradicating SQLi via ORM enforcement, XSS via templating, SSRF via centralized HTTP client
7. **Fuzzing basics** — libFuzzer, AFL++, Atheris (Python), Jazzer (Java), Go fuzzing
8. **Supply chain hygiene** — pinning, signing, SLSA-aware builds
9. **Mentor developers** — secure coding training, security champions program

**Certs to consider:**

- CSSLP (Certified Secure Software Lifecycle Professional)
- OSWE (deeply code-review-focused)
- GIAC GSSP (Java / .NET variants)
- [CTMP: Certified Threat Modeling Professional](https://www.practical-devsecops.com/certified-threat-modeling-professional/?fpr=jassics)

### Senior level (5–8 years)
**Possible job titles:**

- Senior Software Security Engineer
- Lead Product Security Engineer
- Staff Application Security Engineer

**New focus areas:**

1. **Bug class root cause analysis** — turning recurring findings into systemic fixes
2. **Secure framework / SDK design** for internal engineering teams
3. **Reviewing critical design docs (RFCs)** before any code is written
4. **Driving secure SDLC adoption** — policies, gates, dashboards
5. **Vulnerability disclosure programs** internally
6. **Mentoring + hiring** software security engineers
7. **Specialization** — cryptography, sandboxing, memory safety migration (e.g., Rust), or browser/extension security

### Staff / Principal / Architect (8+ years)
**Possible job titles:**

- Principal Software Security Engineer
- Software / Product Security Architect
- Distinguished Security Engineer
- Head of Product Security

**Focus areas:**

- Org-wide secure-by-default platforms
- Migration strategies (e.g., moving codebase from C to Rust/Go)
- Cryptographic strategy, key management, PQC readiness
- Talent strategy, technical hiring bar
- External representation — papers, conference talks, OSS

## Career paths from Software Security

```text
                      Software Security
                              │
       ┌──────────────┬───────┴───────┬──────────────┐
       ▼              ▼               ▼              ▼
   Application    Product Sec     Cryptography   Vulnerability
   Security       Engineer        Engineer       Researcher /
   Engineer                                       Exploit Dev
       │              │               │              │
       ▼              ▼               ▼              ▼
   AppSec Lead   Product Sec     Cryptography   Security
                 Architect       Architect      Researcher
       │
       ▼
  Software / Product Security Architect ──► Distinguished Engineer
```

## Lateral pivots from Software Security
- **→ Application Security / Pentesting** — apply your code skills offensively
- **→ Vulnerability Research / Exploit Dev** — find 0-days in real software
- **→ DevSecOps** — automate the secure patterns you create
- **→ Cryptography Engineering** — specialize even deeper
- **→ Engineering Manager (Security)** — lead a software security team

## AI-augmented Software Security (you need this in 2025+)
AI is rewriting how secure code gets written, reviewed, and exploited.

### Using AI to write more secure code
1. **AI code generation review** — LLM-generated code (Copilot, Cursor, Claude Code) commonly produces vulnerable patterns: SQLi via string concat, missing authz checks, hardcoded secrets, unsafe deserialization, dependency hallucination. Code review for AI-written code is now its own skill.
2. **Custom Semgrep / CodeQL rules with AI** — ask AI to convert CVE patterns into static analysis rules; you still validate the rule
3. **AI-assisted threat modeling** — first-pass STRIDE / attack trees from architecture diagrams or RFCs
4. **CVE root-cause analysis** — paste a patch diff, get the explanation; cross-check with the advisory
5. **Beware hallucinated packages** — "slopsquatting" is when LLMs invent npm / PyPI packages that attackers register. Pin and verify.

### Securing software that embeds AI
1. **OWASP Top 10 for LLM Applications** mapped to your codebase
2. **Insecure plugin / tool design** — agents that call internal APIs need authz checks for the **user**, not just for the agent's service account
3. **Output handling** — LLM output is untrusted input; never directly into eval, shell, SQL, or `dangerouslySetInnerHTML`
4. **Prompt injection defenses** at the framework / library level (LLM-Guard, Rebuff, Guardrails AI, NeMo Guardrails)
5. **Secrets and PII** — designs that don't accidentally feed customer data to third-party model providers
6. **AI-BOM** — track which models, datasets, prompts your software ships, similar to SBOM
7. **Reproducible inference** where business requires it (regulated industries)

See: [AI Security Career Roadmap](ai-security-career-roadmap.md) · [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

## Recommended tools
- **SAST**: Semgrep, CodeQL, SonarQube, Checkmarx, Fortify
- **SCA**: Snyk, Dependabot, OWASP Dependency-Check
- **Fuzzing**: libFuzzer, AFL++, Atheris, Jazzer, OSS-Fuzz
- **Threat modeling**: OWASP Threat Dragon, Microsoft TMT, IriusRisk, pytm

## Recommended books
- *Threat Modeling: Designing for Security* — Adam Shostack
- *Secure by Design* — Daniel Deogun, Dan Bergh Johnsson
- *Designing Secure Software* — Loren Kohnfelder
- *The Tangled Web* — Michal Zalewski
- *Real-World Cryptography* — David Wong
- *Secure Coding in C and C++* — Robert Seacord (if in C/C++ world)

## Next step
Pick one open source project in your favorite language and **submit a security PR** (a CodeQL rule, a hardening, a vulnerable pattern fix). It's the fastest way to get noticed by Software Security hiring managers.
