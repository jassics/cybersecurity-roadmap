# Common or Important Security Concepts that you should be aware of

Every cybersecurity role — analyst, engineer, architect — will quiz you on these in interviews and rely on them daily on the job. Memorize the definitions, but more importantly, learn **why each exists** and **what breaks when it's missing**.

> Tip: For each concept below, try to think of one **real-world example** and one **attack that exploits its absence**. That's how interviewers separate "read about it" from "understands it".

## Common Security Concepts

### CIA Triad
The foundation of all security thinking — every control you'll ever design protects one or more of these:

- **Confidentiality** — only authorized people / systems can see the data. Broken by: data leaks, unencrypted storage, IDOR, sniffing.
- **Integrity** — data has not been altered without authorization. Broken by: tampering, MITM, SQL update injection, unsigned firmware updates.
- **Availability** — data and services are reachable when needed. Broken by: DoS/DDoS, ransomware, accidental outages, deleted backups.

Some frameworks extend this to the **CIA + Authenticity + Non-Repudiation** model (Parkerian Hexad: + Possession/Control and Utility).
### AuthN and AuthZ
Two words that sound similar but mean very different things — confusing them in an interview is a red flag:

- **Authentication (AuthN)** — *Who are you?* Proving identity. Examples: password, OTP, fingerprint, X.509 cert, SSO.
- **Authorization (AuthZ)** — *What are you allowed to do?* Granting permissions. Examples: IAM policies, ACLs, RBAC, ABAC.

Classic pitfall: building strong AuthN but weak AuthZ leads to **IDOR / BOLA** — you know who the user is, but you don't check whether they should access *this specific resource*.
### MFA (Multi-Factor Authentication)
Requiring **two or more** authentication factors from different categories:

1. Something you **know** — password, PIN
2. Something you **have** — phone, hardware token (YubiKey), smart card
3. Something you **are** — fingerprint, face, iris

MFA dramatically reduces account-takeover risk. **Not all MFA is equal**:

- **SMS / Email OTP** — weak (SIM swap, email compromise)
- **TOTP apps** (Google Authenticator, Authy) — strong
- **Push notifications** — strong but vulnerable to MFA fatigue / push bombing
- **FIDO2 / WebAuthn / Passkeys** — strongest; phishing-resistant
### 2FA (Two-Factor Authentication)
A subset of MFA — *exactly two* factors. Every 2FA is MFA, but not every MFA is 2FA (it could be 3FA or more).

In practice, recruiters and product docs use 2FA and MFA interchangeably. Know the technical distinction for interviews.
### OAuth 2.0
An **authorization framework** (not authentication) that lets a user grant a third-party app limited access to resources on their behalf — without sharing the password.

Key actors: **Resource Owner** (user) → **Client** (app) → **Authorization Server** → **Resource Server**.

Grant types you'll see in JDs:

- **Authorization Code** (+ PKCE) — recommended for web + mobile apps
- **Client Credentials** — server-to-server (no user)
- **Device Code** — TVs, CLIs, IoT
- **Implicit & Password** — *deprecated*

Common mistake: treating OAuth 2.0 as an authentication protocol. It isn't — that's what **OIDC** (below) is for.
### SSO (Single Sign-On)
Log in once, access many apps. Implemented via SAML, OIDC, or proprietary identity providers (Okta, Azure AD/Entra ID, Google Workspace, Ping).

Benefits: better UX, fewer passwords to phish, central MFA + offboarding.
Risks: **one compromised account → all SaaS apps** — so SSO accounts must have strong MFA, conditional access, and monitoring.
### OIDC and SAML
Two protocols that handle **federated authentication** — letting an identity provider (IdP) vouch for a user to other apps (SPs / RPs).

- **SAML 2.0** — XML-based; older; very common in enterprise SaaS. Browser POSTs a signed assertion.
- **OIDC (OpenID Connect)** — built on top of OAuth 2.0; JSON / JWT based; the modern choice, especially for mobile and SPAs.

Interview gotchas:

- OIDC adds **identity (ID Token)** on top of OAuth 2.0's **access token**.
- Common vulns: weak signature validation, XML signature wrapping (SAML), JWT `alg=none`, mis-set audience claims, open redirect in callback URLs.
### Malware
Umbrella term for **mal**icious **soft**ware. Includes everything below:

- **Virus** — needs a host file/program; spreads when host is executed
- **Worm** — self-propagating across networks (no host needed)
- **Trojan** — pretends to be legitimate software
- **Ransomware** — encrypts files, demands payment
- **Spyware** — collects info silently
- **Rootkit** — hides itself + provides persistent privileged access
- **Botnet client** — turns the host into a zombie controlled remotely
- **Wiper** — destroys data (no ransom; common in geopolitical attacks)
- **Cryptominer** — uses CPU/GPU to mine crypto for the attacker
### Virus
A specific type of malware that **attaches to a host file or program** and replicates when the host runs. Distinct from a worm (which is self-propagating).

Classic example: macro viruses in Office documents. Modern "viruses" in the news are usually trojans / worms / ransomware misclassified by media.
### Ransomware
Malware that encrypts (or pretends to encrypt) the victim's files and demands payment for the decryption key.

Modern ransomware operators add **double extortion** (also steal data and threaten to leak) and **triple extortion** (DDoS or harass customers). Major families: LockBit, BlackCat/ALPHV, Royal, Akira, Cl0p.

Defense mindset: backup + recovery + segmentation + EDR + email/web filtering + privileged access controls + tabletop exercises.
### Spam and Phishing
- **Spam** — unsolicited bulk messages (usually email). Mostly annoying; sometimes the delivery mechanism for phishing or malware.
- **Phishing** — social engineering attack tricking the victim into revealing credentials, clicking malicious links, or running malicious files. Variants:
  - **Spear phishing** — targeted (specific person/role)
  - **Whaling** — targets executives
  - **Vishing** — voice/phone-based
  - **Smishing** — SMS-based
  - **Quishing** — QR-code-based

Defenses: SPF + DKIM + DMARC, email gateway filtering, user training, FIDO2 (phishing-resistant MFA).
### Social Engineering
Manipulating **people** instead of technology. Often the cheapest way into a target.

Common tactics:

- **Pretexting** — invented scenario ("I'm from IT support…")
- **Phishing** (covered above)
- **Baiting** — leaving infected USB drives in parking lots
- **Tailgating / Piggybacking** — following someone through a badge-secured door
- **MFA fatigue / push bombing** — spamming push prompts until the user approves
- **Business Email Compromise (BEC)** — impersonating an exec to redirect wire transfers

Defenses: security awareness training, verified-callback policies, least privilege, hardware MFA.
### Password Attacks
A family of attacks against authentication:

- **Brute force** — try every possible password
- **Dictionary attack** — try common passwords (rockyou.txt, SecLists)
- **Credential stuffing** — use leaked username/password pairs from other breaches
- **Password spraying** — try a few common passwords across many accounts (evades lockouts)
- **Rainbow tables** — precomputed hashes (defeated by salting)
- **Pass-the-hash / Pass-the-ticket** — Windows-specific; reuse stolen credentials/tickets

Defenses: strong KDFs (bcrypt, argon2, scrypt), salt, rate limiting, MFA, breached-password checks (HIBP), account lockout policies.
### Threats
A **threat** is *anything* that could harm an asset — an actor, action, or event.

Types:

- **Threat actor / agent** — who could attack (state actor, criminal, insider, hacktivist)
- **Threat vector** — how (phishing email, USB drop, exposed service)
- **Threat intelligence** — data about who is targeting whom, how, and why

Threat ≠ Vulnerability ≠ Risk — see [cybersecurity-terminologies.md](cybersecurity-terminologies.md) for crisp definitions.
### Vulnerabilities
A **weakness** in a system, application, process, or person that a threat can exploit.

Lifecycle: **Discovered → Disclosed → Patched → Verified**. Tracked via CVE IDs (cve.mitre.org / NVD). Scored via CVSS (base, temporal, environmental).

Additional scoring systems modern teams use:

- **EPSS** — Exploit Prediction Scoring System (probability of exploitation in next 30 days)
- **CISA KEV** — Known Exploited Vulnerabilities catalog ("patch these now")
- **SSVC** — Stakeholder-Specific Vulnerability Categorization
### Exploits
A piece of code or technique that **takes advantage of a vulnerability** to cause unintended behavior (RCE, privilege escalation, info disclosure, DoS).

- **0-day exploit** — used before the vendor / public know about the vulnerability
- **N-day exploit** — used after a patch is public; preys on slow patchers
- **PoC (Proof of Concept)** — minimal code that proves the bug exists
- **Weaponized exploit** — production-grade, reliable, with delivery mechanism
### Risk
**Risk = Likelihood × Impact** (qualitatively). Or, more formally:

> Risk is the potential for **loss** when a **threat** exploits a **vulnerability** affecting an **asset**.

Risk treatment options (memorize for any GRC interview):

- **Mitigate** — apply controls to reduce likelihood or impact
- **Transfer** — buy insurance, push to a vendor (contractual transfer)
- **Avoid** — stop doing the risky activity entirely
- **Accept** — acknowledge and live with it (with formal sign-off)

Advanced: **FAIR** (Factor Analysis of Information Risk) — quantitative risk in dollars.

## Web Security
### OWASP Top 10 (Web)
The most well-known awareness document in security. Updated every ~3–4 years. The 2021 edition (current at time of writing):

1. A01: Broken Access Control
2. A02: Cryptographic Failures
3. A03: Injection
4. A04: Insecure Design
5. A05: Security Misconfiguration
6. A06: Vulnerable and Outdated Components
7. A07: Identification and Authentication Failures
8. A08: Software and Data Integrity Failures
9. A09: Security Logging and Monitoring Failures
10. A10: Server-Side Request Forgery (SSRF)

Know each category, one example vuln, and one mitigation. Also know **OWASP API Top 10 (2023)** and **OWASP Top 10 for LLM Applications**.
### XSS (Cross-Site Scripting)
Injecting JavaScript into a web page that runs in another user's browser. Three flavors:

- **Reflected** — payload bounces off the server in the response (URL parameter → page)
- **Stored** — payload stored on the server (DB / file) and served to every visitor
- **DOM-based** — payload manipulates the DOM client-side; never touches the server

Impact: session hijacking, credential theft, defacement, cryptojacking, internal SSRF via fetch().

Defenses: context-aware output encoding (HTML / JS / URL / CSS), Content Security Policy (CSP), HttpOnly + Secure + SameSite cookies, trusted-types in modern browsers, input validation as defense-in-depth.
### Injection Attacks
Untrusted user data is interpreted as code/command by the backend. Flavors:

- **SQL Injection (SQLi)** — into a database query
- **NoSQL Injection** — MongoDB, etc.
- **OS Command Injection** — into a shell command
- **LDAP Injection**
- **XML / XPath Injection**
- **Template Injection (SSTI)** — Jinja2, Twig, ERB, Velocity etc.
- **Header Injection / CRLF Injection**
- **Log Injection** — fakes log entries; can lead to Log4Shell-style RCE

Defenses: parameterized queries / prepared statements, allow-lists, ORMs used correctly, sandbox templates, escape on output, principle of least privilege at the DB layer.
### CSRF (Cross-Site Request Forgery)
A malicious site causes the victim's browser to make an **authenticated request** to a target site, without the user's intent.

Classic example: image / form on `evil.com` that POSTs to `bank.com/transfer` while the user is logged in to the bank.

Defenses:

- **CSRF tokens** (synchronizer pattern)
- **SameSite cookies** (`Lax` or `Strict`)
- **Double-submit cookie** pattern
- **Origin / Referer header validation**
- Don't use **state-changing GETs**
### SSRF (Server-Side Request Forgery)
The **server** is tricked into making a request the attacker chooses. Often used to:

- Hit internal services (e.g., `http://localhost:8500/v1/agent/`)
- Hit cloud metadata APIs (`http://169.254.169.254/`) → steal IAM credentials
- Port scan internal networks via timing oracles

Defenses: deny-list metadata IPs (or better, allow-list of known outbound URLs), enforce IMDSv2 in AWS, separate egress proxy, no DNS rebinding (resolve once and use that IP), URL parser strictness.
### HTTP Header / Request Smuggling
A class of attacks where **two HTTP parsers disagree** about where a request ends — typically a frontend proxy/CDN and a backend server.

Variants: CL.TE, TE.CL, TE.TE, plus newer H2.CL / H2.TE in HTTP/2 → HTTP/1.1 downgrade paths.

Impact: bypass front-end controls, poison cache, hijack queued user requests, exfiltrate data.

Defenses: use HTTP/2 end-to-end, reject ambiguous headers, normalize at the edge, strict parsers (PortSwigger's research is the canonical reference).
### Session Fixation
Attacker forces a victim to use a **known session ID**, then waits for the victim to log in — and inherits the authenticated session.

Defense: **regenerate the session ID after authentication** (and after privilege changes). Don't accept session IDs from URLs.

## Application Security

Most AppSec interview questions reduce to a deep variant of one of the OWASP Top 10. In addition, be ready to discuss:

- **Threat modeling** (STRIDE, attack trees, PASTA, DREAD)
- **Secure SDLC** — shift-left, security gates in CI, security champions program
- **Defense in depth** — never rely on a single control
- **Least privilege** — applies to code, services, IAM, DB users, file permissions, and humans
- **Fail securely** — when something errors, default to denied / closed, not allowed / open
- **Secrets management** — don't put secrets in code or images; use Vault / Secrets Manager / SOPS / KMS
- **Logging & monitoring** — log security events (auth, access, errors) without logging sensitive data

## Network Security

Whether you do AppSec, Cloud, or SOC, you'll need to think about networks. Master these protocols and ideas:
### How SSL/TLS Works
TLS provides **confidentiality, integrity, and authentication** for network traffic. The handshake (TLS 1.3) at a high level:

1. Client sends `ClientHello` (supported ciphers, key share for ECDHE)
2. Server sends `ServerHello`, certificate, and signed key share
3. Both derive session keys (no separate RSA key exchange step → forward secrecy is mandatory in TLS 1.3)
4. Application data flows encrypted

Key concepts: cipher suites, certificate chain validation, SNI, ALPN, OCSP / OCSP stapling, certificate transparency, HSTS, certificate pinning (for mobile apps).

Learn more: [howhttps.works](https://howhttps.works/)
### How DNS Works
DNS converts human-friendly names (`example.com`) to IP addresses. Recursive resolution:

`Stub resolver` → `Recursive resolver` → `Root servers (.)` → `TLD servers (.com)` → `Authoritative servers` → answer

Record types you must know: A, AAAA, CNAME, MX, NS, SOA, TXT, PTR, SRV, CAA.

Security concepts:

- **DNSSEC** — adds signatures to records (integrity + authenticity, not confidentiality)
- **DoH / DoT / DoQ** — DNS over HTTPS / TLS / QUIC (confidentiality)
- **Cache poisoning** — see below
- **Subdomain takeover** — dangling CNAME to a service that's been deleted

Learn more: [howdns.works](https://howdns.works/)
### TCP 3-Way Handshake
How a TCP connection is established between two hosts:

```text
Client                                Server
  │   ────  SYN  (seq=x)         ───►  │
  │ ◄───  SYN+ACK (seq=y, ack=x+1) ──  │
  │   ────  ACK  (ack=y+1)       ───►  │
  │                                    │
  │       connection ESTABLISHED       │
```

Attacks built on this:

- **SYN flood** — never send the final ACK; server keeps half-open connections (mitigated by SYN cookies)
- **TCP reset injection** — attacker spoofs RST packets to tear down a session
- **Idle scan (nmap -sI)** — abuses predictable IP IDs of a "zombie" host
### Firewall
A device or software that controls network traffic based on rules. Evolution:

- **Packet filter** — looks at headers only (L3/L4)
- **Stateful firewall** — tracks connections (replies, ESTABLISHED state)
- **Application-layer / proxy firewall** — understands HTTP, FTP, etc.
- **Next-Generation Firewall (NGFW)** — adds IDS/IPS, app awareness, user identity (e.g., Palo Alto, Fortinet)
- **Web Application Firewall (WAF)** — focuses on HTTP-layer attacks (Cloudflare, AWS WAF, ModSecurity)
- **Cloud-native**: AWS Security Groups + NACL, Azure NSG, GCP firewall rules

Most firewalls fail because of overly permissive rules, not because the product is bad.
### DoS and DDoS
- **DoS (Denial of Service)** — one source overwhelms a target
- **DDoS (Distributed)** — many sources (botnet, IoT devices, amplification)

Layers attacked:

- **L3/L4 volumetric** — UDP flood, SYN flood, amplification (DNS, NTP, memcached, SSDP)
- **L7 application** — HTTP flood, slowloris, expensive endpoints

Defenses: CDN + scrubbing centers (Cloudflare, Akamai, AWS Shield), rate limiting, captchas, BGP blackholing for severe cases.
### Ping Flood
A simple DoS where the attacker sends ICMP Echo Requests (`ping`) faster than the target can respond. Modern OSes and edge devices handle this trivially, but it's a useful training concept.

Variant: **Smurf attack** — spoof the victim's IP and ping a broadcast address; all hosts reply to the victim (largely mitigated by disabling directed broadcasts).
### Cache Poisoning
Tricking a cache to store malicious or unintended content, served to subsequent users.

Variants:

- **DNS cache poisoning** — inject forged DNS responses (mitigated by source-port randomization, DNSSEC)
- **Web cache poisoning** — abuse unkeyed headers (`X-Forwarded-Host`, etc.) to make CDNs serve attacker-controlled content (PortSwigger James Kettle's research is canonical)
- **HTTP/2 stream cache poisoning** — newer variant

## Cloud Security

Know these by heart before any cloud security interview:

### Shared Responsibility Model
The cloud provider secures **of** the cloud; you secure **in** the cloud.

| Layer | IaaS (EC2) | PaaS (RDS) | SaaS (M365) |
|-------|------------|------------|-------------|
| Customer data | You | You | You |
| Apps / OS | You | Provider | Provider |
| Network controls | You | Shared | Provider |
| Hypervisor / Hardware | Provider | Provider | Provider |

It is **always your job** to: configure identity, classify data, secure your apps, manage your secrets, watch your logs.
### IAM (Identity & Access Management)
Who can do what to which resource. The cloud's most-attacked surface.

Core primitives (AWS example, others are similar):

- **Users / Groups / Roles** — identities
- **Policies** — JSON documents granting/denying actions on resources
- **Trust policies** — *who is allowed to assume this role*
- **Permission boundaries / SCPs** — guardrails that cap maximum permissions
- **Federation / SSO** — bring your IdP into cloud IAM

Common mistakes: `*:*` policies, overly broad trust policies (`Principal: *`), long-lived access keys instead of roles, missing MFA on root.
### CSPM (Cloud Security Posture Management)
Continuously checks your cloud config against benchmarks (CIS, NIST, custom) and flags drift.

Tools: Wiz, Prisma Cloud, Defender for Cloud, Lacework, Orca, Snyk Cloud, Prowler (open source).
### CASB (Cloud Access Security Broker)
A control plane that sits between users and **SaaS apps** to enforce policy, DLP, threat detection, and visibility. Useful for SaaS sprawl (Shadow IT).

Tools: Netskope, Microsoft Defender for Cloud Apps, Zscaler, McAfee MVISION.
### CWPP (Cloud Workload Protection Platform)
Protects workloads — VMs, containers, serverless — at runtime. Vulnerability management + behavior monitoring + EDR-like alerts.

Often consolidated with CSPM + CIEM + DSPM into a single **CNAPP** (Cloud-Native Application Protection Platform). Tools: Wiz, Prisma Cloud Defender, Aqua, Sysdig Secure.

## Cryptography

You don't need to design ciphers, but every security engineer must understand how to *use* them correctly. **Never roll your own crypto.**

### Encryption and Decryption
Converting plaintext to ciphertext (and back) using a key.

- **Symmetric** — same key both sides. Fast. Examples: AES-GCM, ChaCha20-Poly1305
- **Asymmetric** — public/private key pair. Slow. Examples: RSA, ECDSA, Ed25519
- **Hybrid** — use asymmetric to exchange a symmetric key, then encrypt bulk data symmetrically (how TLS works)

Common mistakes: ECB mode ("looks like the plaintext"), reusing IVs in CTR/GCM, hardcoded keys in source, no key rotation.
### Hashing
One-way function: data → fixed-size digest. Same input → same output. Can't reverse.

Used for: data integrity, signatures, deduplication, password storage (with KDFs).

- **Strong general-purpose**: SHA-256, SHA-3, BLAKE3
- **For passwords**: **bcrypt**, **scrypt**, **Argon2** (slow / memory-hard on purpose)
- **Broken / weak**: MD5, SHA-1 (don't use except for non-security checksums)

Classic interview question: "Why is SHA-256 *bad* for storing passwords?" Answer: it's too fast → attackers can brute-force billions per second on GPUs. Use a KDF (above).
### Encoding and Decoding
**Encoding is not encryption.** It's a reversible transformation with no secret.

Examples: Base64, hex, URL encoding, HTML entity encoding.

Use cases: transporting binary safely over text protocols, escaping output for a specific context.

Interview trap: "This password is encrypted in Base64" — *no, it's encoded*. Anyone can decode it instantly.
### Salt
A unique random value added to a password **before hashing**, stored alongside the hash.

Why: defeats rainbow tables and ensures two users with the same password get different hashes.

Modern password storage = `Argon2id(password, salt, params)` — the KDF generates and manages the salt for you.

Related concepts:

- **Pepper** — a *secret* value added like a salt, but stored separately (e.g., in an HSM / env var). Adds defense-in-depth.
- **Nonce / IV** — "number used once" for encryption modes; never reuse with the same key.

---

## Going further

For a quick reference of acronyms and terms used above, see:

- [cybersecurity-abbreviations.md](cybersecurity-abbreviations.md)
- [cybersecurity-terminologies.md](cybersecurity-terminologies.md)

For how each of these concepts maps to job roles, see [security-job-roles.md](security-job-roles.md).
