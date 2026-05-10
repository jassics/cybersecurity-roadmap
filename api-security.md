# API Security Skills and Career Roadmap

> 📘 Recommended study plans: [Secure Code Review](https://github.com/jassics/security-study-plan/blob/main/secure-code-review-study-plan.md) · [Product Security](https://github.com/jassics/security-study-plan/blob/main/product-security-study-plan.md).

API Security has emerged as its own specialty over the last 5 years. Modern apps are *mostly* APIs — mobile apps, SPAs, microservices, B2B integrations all expose APIs. Attackers know this; OWASP gave it a dedicated Top 10.

> If you're starting fresh, do [web-security.md](web-security.md) first. API security is best learned **after** OWASP Web Top 10.

## Who is this for?
- AppSec / Web Pentesters wanting to specialize
- Backend developers moving into security
- DevSecOps engineers responsible for API gateways

## Pre-requisites
1. HTTP fundamentals (methods, headers, status codes, content negotiation)
2. JSON / XML / YAML / Protobuf basics
3. REST principles + understanding of RPC, GraphQL, gRPC, WebSockets
4. AuthN/AuthZ — sessions, JWT, OAuth2, OIDC, mTLS, API keys
5. At least one programming language for writing PoCs
6. OWASP Web Top 10 understanding

## Career ladder

### Entry level (0–2 years in security)
**Possible job titles:**

- API Security Analyst (rare standalone; usually under AppSec)
- Application Security Analyst (API-leaning)
- Web/API Pentester (Junior)

**Skills to focus on:**

1. **OWASP API Security Top 10 (2023)** — BOLA, Broken Auth, BOPLA, Unrestricted Resource Consumption, BFLA, Unrestricted Access to Sensitive Business Flows, SSRF, Security Misconfiguration, Improper Inventory Management, Unsafe Consumption of APIs
2. **Burp Suite** — handling JSON, REST, modifying requests at scale
3. **Postman / Insomnia / Bruno** — building and replaying API collections
4. **Authentication flows** — JWT pitfalls (alg=none, weak secrets, kid injection), OAuth2 misconfigs
5. **Recon for APIs** — Swagger/OpenAPI discovery, JS file analysis, Kiterunner, ffuf for API endpoints
6. **GraphQL testing** — introspection, batch attacks, depth/complexity DoS
7. **Rate limit / business logic** testing
8. Writing **API-specific PoC scripts** in Python (httpx, requests)

### Mid level (2–5 years)
**Possible job titles:**

- API Security Engineer
- Senior AppSec Engineer (API focus)
- API Penetration Tester

**New skills to add:**

1. **API Gateway security** — Kong, Apigee, AWS API Gateway, Azure APIM, Tyk
2. **WAF for APIs** — Cloudflare API Shield, Akamai, Wallarm, Salt Security
3. **gRPC, GraphQL deep dive** — schema review, federation security
4. **Service mesh** authorization (Istio, Linkerd)
5. **mTLS** and certificate-based auth
6. **API discovery / inventory tools** — Salt, Noname, 42Crunch, Traceable
7. **SAST for APIs** — Spectral (Stoplight) for OpenAPI linting; Semgrep rules for API patterns
8. **DAST for APIs** — APIsec, 42Crunch scan, ZAP API scan, Schemathesis
9. **Designing secure APIs** — pagination, idempotency, signing requests, replay protection

**Certs to consider:**

- [CASP: Certified API Security Professional](https://www.practical-devsecops.com/certified-api-security-professional/?fpr=jassics)
- Burp Suite Certified Practitioner
- OSWE (code-heavy, API-relevant)

### Senior level (5–8 years)
**Possible job titles:**

- Senior API Security Engineer
- API Security Architect
- Product Security Engineer (API specialist)

**New focus areas:**

1. **API security strategy** — discovery + posture + runtime + testing
2. **Threat modeling APIs** — abuse cases, business logic attacks
3. **Zero Trust for APIs** — workload identity, SPIFFE/SPIRE
4. **API governance** — design standards, OpenAPI as source of truth
5. **Bug bounty / responsible disclosure** program for APIs
6. **Cross-functional influence** with platform and product teams

### Staff / Architect (8+ years)
**Possible job titles:**

- API Security Architect
- Principal Product Security Engineer (API)

**Focus areas:**

- API security at scale (10k+ endpoints)
- Vendor strategy (API security platform vs. CNAPP)
- Mentoring AppSec teams; org-wide standards

## Career paths from API Security

```text
                      API Security
                            │
       ┌────────────────────┼────────────────────┐
       ▼                    ▼                    ▼
  AppSec / Product      DevSecOps (API       Cloud Security
  Security Engineer     pipeline focus)      (gateway focus)
       │                    │                    │
       ▼                    ▼                    ▼
  Security Architect    Platform Sec        Cloud Security
                        Engineer            Architect
```

## Lateral pivots
- **→ Web Security / AppSec** — broader application surface
- **→ Cloud Security** — APIs live in the cloud
- **→ DevSecOps** — automate API testing
- **→ Mobile Security** — mobile apps are mostly API clients
- **→ Bug bounty** — API bugs pay well and are common

## AI-augmented API Security (you need this in 2025+)
AI both **drives** and **threatens** modern APIs.

### Using AI to do API security better
1. **AI-assisted OpenAPI / Postman analysis** — prompt to map endpoints to OWASP API Top 10 risk categories
2. **Schema fuzzing with AI** — generate edge-case payloads from an OpenAPI spec
3. **GraphQL schema review** — let AI walk through introspection and surface risky resolvers
4. **Burp / Caido AI extensions** — first-pass triage of large traffic captures
5. **Spec drift detection** — compare OpenAPI to live traffic with AI; flag undocumented endpoints (shadow APIs)

### Securing AI APIs (LLM endpoints, agent tool APIs)
LLM endpoints are now first-class APIs. They need:

1. **AuthN/AuthZ per user**, not per service account; agents should not bypass user authorization
2. **Rate limiting + token budgets** — prompt injection-driven token amplification attacks
3. **Input validation** — max prompt length, structure, allowed tools / functions
4. **Output validation** — schema-validate JSON output, sanitize before downstream use
5. **PII / DLP filters** at the gateway
6. **Provenance + audit logging** — store prompt, completion, tool calls; expect e-discovery requests
7. **Tool / function call authorization** — if the agent can call `deleteUser`, who gets to authorize?

See: [AI Security Career Roadmap](ai-security-career-roadmap.md) · [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

## Recommended tools
- **Testing**: Burp Suite (+ Hackvertor, Logger++, JWT Editor), Postman, Bruno, ffuf, Kiterunner, mitmproxy, Caido
- **GraphQL**: GraphQL Voyager, InQL, graphql-cop, clairvoyance
- **OpenAPI**: Spectral, openapi-diff, 42Crunch CLI
- **Discovery / posture**: Salt Security, Noname, Traceable, Akto (open source)

## Recommended resources
- [OWASP API Security Top 10](https://owasp.org/API-Security/)
- [APIsec University (free)](https://www.apisecuniversity.com/)
- *Hacking APIs* — Corey J. Ball
- Inon Shkedy's API security checklist (GitHub)

## Next step
Set up [crAPI](https://github.com/OWASP/crAPI) and [VAmPI](https://github.com/erev0s/VAmPI) locally. Try to find every OWASP API Top 10 issue manually before reaching for a scanner.
