# Cryptography Engineering Career Roadmap

> 📘 Recommended study plans: [Common Skills](https://github.com/jassics/security-study-plan/blob/main/common-skills-study-plan.md) · [Product Security](https://github.com/jassics/security-study-plan/blob/main/product-security-study-plan.md) · [Secure Code Review](https://github.com/jassics/security-study-plan/blob/main/secure-code-review-study-plan.md).

Cryptography Engineering is a **specialized, math-flavored, deeply technical** corner of cybersecurity. It is one of the **smallest career tracks by headcount**, but consistently among the **best paid** because qualified people are rare and the cost of mistakes is catastrophic (think Heartbleed, Dual_EC_DRBG, ROBOT, Logjam, Padding Oracle). Most companies don't *invent* cryptography — but every product company needs at least a few people who can **integrate, review, and operate** it correctly.

> **Important distinction:**
> - **Cryptographer / Cryptanalyst (research)** — invents and breaks algorithms. PhD-level math, mostly academia / NIST / national labs / vendors like Microsoft Research, Cloudflare Research, IBM Research.
> - **Cryptography Engineer (this roadmap)** — applies, integrates, reviews, and runs cryptographic systems. Strong CS + math + security background; **does not require a PhD**.

This roadmap focuses on **Cryptography Engineering**. The research path is briefly noted at the end.

## Who is this for?
- AppSec / software engineers fascinated by crypto bugs and protocol design
- Security engineers in BFSI, payments, identity, blockchain, or messaging
- Cloud security engineers handling KMS / HSM / key lifecycle at scale
- People who *enjoyed* the cryptography sections of CTFs and want to do that for a living
- Folks aiming for niche, hard-to-replace, well-compensated roles

## Pre-requisites (foundation)
1. Strong programming — at least one of C, Rust, Go, Java, or Python (with crypto libs)
2. Computer architecture basics — endianness, memory, timing, side channels
3. Discrete math basics — modular arithmetic, group theory at high level, basic number theory
4. Linear algebra and probability (high-school+ level enough to start)
5. Networking + TLS at the level of *Bulletproof TLS and PKI* (Ivan Ristić)
6. Solid understanding of common AppSec issues — you'll review code that uses crypto wrong
7. Comfort reading RFCs, NIST SPs, and academic papers

## What to learn (core crypto knowledge)

### Symmetric crypto
- Block ciphers — AES (modes: ECB never, CBC, CTR, GCM, GCM-SIV, XTS for disk)
- Stream ciphers — ChaCha20, ChaCha20-Poly1305 (AEAD)
- Hash functions — SHA-2, SHA-3, BLAKE2/3
- MACs — HMAC, KMAC, Poly1305
- KDFs — HKDF, PBKDF2, scrypt, Argon2 (password hashing)
- AEAD — why nonce reuse breaks GCM; misuse-resistant constructions

### Asymmetric crypto
- RSA (PKCS#1 v1.5 vs OAEP, PSS); why textbook RSA is broken
- Elliptic curves — P-256, P-384, Curve25519, Ed25519, secp256k1
- Diffie-Hellman, ECDH, X25519
- Signatures — ECDSA, EdDSA, RSA-PSS
- Key exchange and forward secrecy

### Protocols & systems
- **TLS 1.2 vs 1.3** in depth — handshake, ciphersuites, key schedule
- **Noise Protocol Framework** (used by WireGuard, WhatsApp)
- **Signal Protocol** (X3DH + Double Ratchet)
- **Kerberos** and PKI (X.509, OCSP, CT logs)
- **JWT / JWS / JWE / JWK** — and why JWT is mis-designed in many ways
- **PASETO**, **Macaroons**, **Biscuit** — modern token alternatives
- **OAuth 2.1 + OIDC** crypto pieces (DPoP, mTLS-bound tokens)

### Key management
- KMS — AWS KMS, GCP KMS, Azure Key Vault, HashiCorp Vault, GCP Confidential Space
- HSM — Thales Luna, AWS CloudHSM, Entrust nShield, YubiHSM
- Standards — FIPS 140-2 / 140-3, Common Criteria (CC EAL)
- Envelope encryption, key wrapping, key rotation, BYOK / HYOK
- Secrets management vs key management (different problems)

### Post-Quantum Cryptography (PQC) — *now mainstream*
This is **the** big shift in 2024–2030. NIST finalized:

- **ML-KEM (Kyber)** — key encapsulation
- **ML-DSA (Dilithium)** — digital signatures
- **SLH-DSA (SPHINCS+)** — stateless hash-based signatures
- **FN-DSA (Falcon)** — short-signature alternative

Topics to know:

- Hybrid key exchange (ECDH + ML-KEM)
- Crypto agility — designing systems so algorithms can be swapped
- "Harvest now, decrypt later" threat model
- CNSA 2.0 timelines, BSI / ANSSI guidance
- TLS 1.3 PQ — Cloudflare, Google, AWS rollouts

### Side-channel & implementation security
- Timing attacks — constant-time programming, `crypto/subtle` style APIs
- Cache attacks (FLUSH+RELOAD, PRIME+PROBE)
- Power / EM analysis (relevant for embedded / IoT / HSM design)
- Fault injection
- Speculative execution (Spectre / Meltdown family)
- Why never roll your own crypto — and what *integrating* it correctly looks like

### Specialized areas
- **Privacy-Enhancing Technologies (PETs)** — differential privacy, secure multiparty computation, homomorphic encryption (FHE), zero-knowledge proofs (zk-SNARK / zk-STARK)
- **Confidential Computing** — Intel SGX, AMD SEV-SNP, ARM CCA, Nitro Enclaves
- **Blockchain crypto** — secp256k1, BLS, Schnorr, threshold signatures, MPC wallets

## Career ladder

### Entry — Junior Cryptography / Applied Security Engineer (0–2 yrs in crypto, 2–4 yrs total)
*Most people enter from AppSec, software engineering, or backend.*

**Typical work**

- Implement cryptographic features under guidance (mTLS, JWT signing, HMAC, payload encryption)
- Code-review libraries' usage — catch ECB, hardcoded IVs, weak KDFs, custom crypto
- Integrate KMS / Vault into services
- Write threat models for crypto-using features

**Skills**

- Strong language (Go / Rust / Java / C / Python) + a major crypto lib (libsodium, BoringSSL, Tink, ring, RustCrypto)
- Solid TLS 1.2/1.3, certificate handling
- Comfortable with at least AWS KMS or GCP KMS or Vault
- *Cryptography I (Boneh, Coursera)* completed

### Mid — Cryptography Engineer (3–6 yrs total)
**Typical work**

- Design crypto components — token formats, encrypted storage, signed audit logs
- Build internal libraries / SDKs that wrap primitives so other engineers can't misuse them
- Lead crypto reviews across the org
- Drive HSM / KMS architecture decisions
- Run incident response on crypto-related findings (downgrade attacks, weak ciphersuites, expired certs)

**Skills**

- Deep TLS, PKI, key management
- Read RFCs and NIST SPs fluently
- Build constant-time, side-channel-aware code
- Strong AppSec foundation
- Familiarity with PQC roadmap and crypto agility patterns

### Senior — Senior Cryptography Engineer (6–10 yrs)
**Typical work**

- Own crypto across an entire product line / platform
- Design end-to-end-encrypted features (E2EE messaging, encrypted backups, sealed sender)
- Drive PQC migration program org-wide
- Speak at conferences (Real World Crypto, USENIX Security, Black Hat)
- Mentor mid-level engineers; set crypto coding standards

**Skills**

- Protocol design experience (Noise, Signal-style ratchets, custom AEAD constructions when justified)
- Confidential Computing or HSM-deep work
- Public-facing voice — blog posts, RFC contributions, open-source maintenance

### Staff / Principal — Principal Cryptography Engineer (10+ yrs)
**Typical work**

- Define crypto strategy across multiple BUs
- Drive standardization with external bodies (IETF, NIST, CA/B Forum)
- Architect E2EE / PQC / Confidential Compute platforms
- Be the org's "Court of Last Appeal" on crypto questions

**Where these jobs exist**

- Hyperscalers (AWS / Google / Microsoft / Apple)
- Payment / fintech (Stripe, Square, Visa, Mastercard, banks)
- Messaging / privacy (Signal, WhatsApp, Apple)
- Cloud-native security vendors (Cloudflare, HashiCorp, Hashi, Sigstore)
- Web3 / blockchain infrastructure (Coinbase, Chainlink, zk-rollup teams)
- Government / defense / national labs

## Specialization branches

### PQC migration specialist
- Help orgs inventory cryptographic assets, pilot hybrid TLS, migrate signing systems
- Hot in 2025–2030; many BFSI / government mandates
- Tools: open-quantum-safe (OQS), liboqs, Cloudflare's CIRCL

### Confidential Computing engineer
- SGX / SEV-SNP / TDX / Nitro Enclaves
- Attestation, sealed storage, multi-party AI workloads on encrypted data
- Strong overlap with AI security (private inference, federated learning)

### Blockchain / Web3 cryptography
- Threshold signatures (TSS), MPC wallets, BLS aggregation, zero-knowledge circuits
- Custodian / exchange / L2 infra

### Privacy engineering
- Differential privacy, federated learning, FHE, MPC, zk-proofs for compliance and analytics
- Hybrid GRC + Crypto + AppSec role

### Cryptographer / Cryptanalyst (research)
- PhD path; algorithm design, formal analysis, attack publication
- Research labs (Microsoft Research, IBM, Cloudflare, Inria, ENS, MPI)

## Career paths from Cryptography Engineering

```text
                AppSec / SWE / Backend Engineer
                              │
                              ▼
                Junior Cryptography Engineer
                              │
                              ▼
                  Cryptography Engineer
              ┌───────────────┼────────────────┐
              ▼               ▼                ▼
        Senior Crypto    PQC Migration    Confidential
         Engineer          Specialist     Computing Eng
              │                │                │
              └────────┬───────┴────────┬───────┘
                       ▼                ▼
              Principal Cryptography  Privacy Engineer
                  Engineer            (PETs / FHE / DP)
                       │                       │
                       ▼                       ▼
              Distinguished Engineer    Web3 / Blockchain
              / Security Architect      Crypto Lead
                       │
                       ▼
                Researcher / Cryptographer
                  (PhD-track / labs)
```

## Lateral pivots from / into Cryptography Engineering
- **AppSec → Crypto Engineering** — the most common path
- **Backend SWE → Crypto Engineering** — if you've worked on auth / tokens / payment systems
- **Crypto → Security Architect** — protocol design experience translates well
- **Crypto → Confidential Computing / Privacy Engineering**
- **Crypto → AI Security** — secure aggregation, federated learning, private inference

## AI-augmented Cryptography Engineering (2025+)
AI is **especially dangerous** here — crypto is one of the fields where LLMs hallucinate plausibly wrong code most often.

### Using AI carefully
1. **Code review prompts** — paste a function and ask for misuse patterns; cross-check against the spec
2. **RFC / NIST SP summarization** — great for first pass; never quote verbatim without re-reading
3. **Generating *test vectors*** — ask AI for KAT-style inputs from RFC appendices to seed property-based tests
4. **Formal threat model first drafts** — STRIDE-style around a crypto component
5. **PQC migration discovery** — feed source / dependency manifests to AI to flag legacy crypto

### Red flags
1. **AI-generated crypto code** — almost always wrong on padding, IV handling, constant-time, or AEAD usage. Treat as a hint, never as final code.
2. **Side-channel reasoning** — LLMs are weak here; involve a human expert.
3. **Custom protocols** — never let an LLM design one for you.

### Securing AI workloads
- Confidential inference (Nitro Enclaves, Intel TDX) — direct overlap with this track
- Secure aggregation in federated learning (Bonawitz et al.)
- Watermarking + signed model artifacts (Sigstore for models)

See: [AI Security Career Roadmap](ai-security-career-roadmap.md) · [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

## Recommended tools / libraries to know
- **High-level libs**: libsodium, Google Tink, AWS Encryption SDK, age
- **Low-level libs**: BoringSSL, OpenSSL, ring (Rust), RustCrypto, Bouncy Castle
- **PQC**: liboqs / open-quantum-safe, CIRCL, pq-crystals
- **KMS / HSM**: AWS KMS + CloudHSM, GCP KMS, Azure Key Vault, HashiCorp Vault, Thales Luna, YubiHSM, SoftHSM (lab)
- **Test / fuzz**: Wycheproof test vectors, AFL/libFuzzer for crypto code
- **Confidential Computing**: Open Enclave SDK, Gramine, Constellation, Microsoft CCF

## Recommended labs / resources
- [Cryptopals Crypto Challenges](https://cryptopals.com/) — *the* gold standard intro
- [CryptoHack](https://cryptohack.org/) — modern, gamified
- *Real World Crypto* conference YouTube channel
- IETF mailing lists — TLS WG, CFRG
- NIST PQC project pages and standards (FIPS 203 / 204 / 205)
- *A Graduate Course in Applied Cryptography* — Boneh & Shoup (free PDF)

## Recommended books
- *Serious Cryptography* — Jean-Philippe Aumasson (best modern intro)
- *Cryptography Engineering* — Ferguson, Schneier, Kohno
- *Bulletproof TLS and PKI* — Ivan Ristić
- *Real-World Cryptography* — David Wong
- *The Code Book* — Simon Singh (history / motivation)
- *Handbook of Applied Cryptography* — Menezes, van Oorschot, Vanstone (free, dense, reference)
- *Post-Quantum Cryptography* — Bernstein, Buchmann, Dahmen (eds.)

## Certifications (limited, but useful)
- **(ISC)² CISSP** — broad, useful for senior roles
- **EC-Council ECES** — Encryption Specialist (entry-level signal)
- **Cloud KMS specialty** — vendor-specific (AWS Security Specialty, Google PCSE)
- **Practical DevSecOps CDP / CDE** — for the AppSec + Crypto integration angle
- *No widely-respected dedicated crypto-engineer cert exists.* Public open-source contribution + a strong blog matter more.

## Recommended creators / blogs to follow
- **A Few Thoughts on Cryptographic Engineering** — Matthew Green
- **Cloudflare Research blog**
- **Trail of Bits blog** (crypto reviews are gold)
- **Filippo Valsorda** (filippo.io) — Go crypto + PQC commentary
- **NCC Group Cryptography Services** — published reviews
- **Real World Crypto** YouTube channel

## Common pitfalls (what employers want you NOT to do)
1. Roll your own crypto / "improve" a standard
2. Use ECB anywhere
3. Use the same nonce twice with GCM
4. Use MD5 / SHA-1 / RC4 / DES for anything new
5. Confuse encryption with authentication (use AEAD)
6. Use `==` to compare MACs (constant-time required)
7. Bake algorithm choice into a binary format with no version field (no crypto agility)
8. Trust JWT defaults blindly (none-alg, alg confusion, key confusion)
9. Hardcode keys in source / mobile apps / containers
10. Ship without an inventory of where crypto is used (you can't migrate to PQC if you can't find it)

## Next step
Pair this roadmap with the [AppSec / Software Security roadmap](software-security.md) — most crypto engineering jobs are filled by strong AppSec engineers who specialized. If you want the math-research path, plan for a PhD; if you want the engineering path, build a public portfolio of crypto reviews + open-source contributions.

Companion JDs: cryptography roles often live inside **[Software Security JDs](JDs/software-security.md)** and **[Security Architect JDs](JDs/security-architect.md)**.
