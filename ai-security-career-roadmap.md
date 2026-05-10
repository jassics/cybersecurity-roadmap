# AI / ML Security Career Roadmap

> 📘 Recommended study plans: [GenAI Security](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md) · [Product Security](https://github.com/jassics/security-study-plan/blob/main/product-security-study-plan.md) · [Common Skills](https://github.com/jassics/security-study-plan/blob/main/common-skills-study-plan.md).

AI Security is the **newest** and one of the hottest areas of cybersecurity. With every company adopting LLMs, AI agents, and ML pipelines, demand for engineers who can secure them has exploded. This space is so new that **even mid-level experience can land you senior roles** if you can prove skill.

Two distinct sub-domains exist:

1. **Security FOR AI** — protecting AI/ML systems from attacks (prompt injection, model theft, training data poisoning).
2. **AI FOR Security** — using LLMs/ML to build detection, triage, and pentest tools (a.k.a. AI-augmented security).

This roadmap focuses primarily on **Security FOR AI**, but most roles will touch both.

## Who is this for?
- AppSec / Cloud / DevSecOps engineers wanting to ride the AI wave
- ML / Data engineers who want a security-flavored career
- Pentesters wanting to specialize in LLM / agent red teaming
- GRC professionals interested in AI governance

## Pre-requisites
1. **Solid security base** in at least one domain (AppSec, Cloud, or DevSecOps)
2. **Python** strong — most ML tooling is Python
3. **ML fundamentals** — supervised/unsupervised, train/test splits, overfitting, embeddings, vector databases (basic understanding is enough to start)
4. **LLM basics** — tokens, context windows, system prompts, RAG, function calling, agents
5. **API security** — almost all AI is consumed via APIs
6. **Cloud basics** (especially SageMaker, Bedrock, Vertex AI, Azure OpenAI)

## Career ladder

### Entry level (0–2 years in AI security; usually 2+ years in adjacent security)
**Possible job titles:**

- AI/ML Security Analyst
- Junior AI Security Engineer
- LLM Red Teamer (Junior)
- Responsible AI / AI Governance Analyst

**Skills to focus on:**

1. **OWASP Top 10 for LLM Applications** — prompt injection, insecure output handling, training data poisoning, model DoS, supply chain, sensitive info disclosure, insecure plugin design, excessive agency, overreliance, model theft
2. **MITRE ATLAS** — adversarial ML threat matrix
3. **Prompt injection deep dive** — direct, indirect, multi-modal (image / audio); tools like PromptInject, Garak
4. **Jailbreaks** — DAN-style, role-play, encoded payloads, ASCII art jailbreaks
5. **LLM API hardening** — rate limits, content filters, output sanitization
6. **Vector DB security** — pgvector, Pinecone, Weaviate, Chroma access controls
7. **RAG-specific risks** — poisoned documents, citation attacks, embedding inversion
8. **AI usage governance** — shadow AI, data exfiltration via copy-paste into ChatGPT, DLP

### Mid level (2–5 years in AI security)
**Possible job titles:**

- AI Security Engineer
- ML Security Researcher
- LLM Red Team Engineer
- MLSecOps Engineer

**New skills to add:**

1. **Adversarial ML** — evasion, poisoning, model inversion, membership inference, model extraction
2. **AI red teaming methodology** — structured campaigns, harm taxonomies (NIST AI RMF, OWASP)
3. **Agent security** — securing autonomous agents (LangChain, LangGraph, AutoGen, CrewAI), tool misuse, infinite loops
4. **Model supply chain security** — HuggingFace model scanning, pickle deserialization risks, ModelScan, Protect AI tooling
5. **Securing MLOps pipelines** — MLflow, Kubeflow, SageMaker, Vertex AI hardening
6. **Privacy techniques** — differential privacy, federated learning basics, PII redaction
7. **AI guardrail frameworks** — NeMo Guardrails, Guardrails AI, LLM-Guard, Rebuff
8. **AI compliance** — EU AI Act, NIST AI RMF, ISO/IEC 42001, India DPDP Act
9. **Threat modeling AI systems** — STRIDE adapted for ML, PAIR framework

**Certs to consider:**

- [CAISP: Certified AI Security Professional](https://www.practical-devsecops.com/certified-ai-security-professional/?fpr=jassics)
- ISC2 / ISACA AI security courses (newer offerings)
- Cloud-specific AI/ML certs (AWS ML Specialty, Azure AI Engineer) for context

### Senior level (5–8 years)
**Possible job titles:**

- Senior AI Security Engineer
- AI Red Team Lead
- AI Security Architect
- Principal MLSecOps Engineer

**New focus areas:**

1. **AI security strategy** for the organization
2. **Threat modeling AI products end-to-end** — training, deployment, inference, telemetry
3. **AI incident response** — what does an "AI incident" even look like?
4. **AI bug bounty programs**
5. **Cross-functional partnership** with data science, legal, ML platform teams
6. **AI risk frameworks** at scale — NIST AI RMF, ISO 42001 implementation
7. **Research & publications** — talks at Black Hat AI Summit, DEF CON AI Village

### Staff / Principal (8+ years overall, 3+ in AI)
**Possible job titles:**

- Principal AI Security Engineer
- AI Security Architect
- Head of AI Security / Responsible AI
- Director of AI Trust & Safety

## Career paths from AI Security

```text
                       AI/ML Security
                              │
       ┌──────────────┬───────┴───────┬──────────────┐
       ▼              ▼               ▼              ▼
   AI Red Team /   MLSecOps        AI Governance /  AI-for-Security
   LLM Pentester   Engineer        Responsible AI   Tooling Engineer
       │              │               │              │
       ▼              ▼               ▼              ▼
   AI Security    Platform Sec    AI Risk Manager  Detection Eng.
   Researcher     Engineer        / DPO+AI hybrid  (LLM-powered)
       │
       ▼
   AI Security Architect ──► Head of AI Trust & Safety
```

## Lateral pivots from AI Security
- **→ Application Security** — most AI is shipped as an app feature
- **→ Cloud Security** — AI workloads live in cloud (Bedrock, Vertex, OpenAI)
- **→ DevSecOps / MLSecOps** — pipeline security for ML
- **→ Privacy Engineering** — overlap with model privacy
- **→ GRC / Responsible AI** — policy + risk side

## Recommended tools
- **LLM red teaming**: Garak (NVIDIA), PyRIT (Microsoft), Promptfoo, DeepEval, llm-attacks
- **Model scanning**: ModelScan, Protect AI, HiddenLayer
- **Guardrails**: NeMo Guardrails, LLM-Guard, Guardrails AI, Rebuff
- **Adversarial ML**: ART (Adversarial Robustness Toolbox), CleverHans, Foolbox
- **MLSecOps**: MLflow security, Giskard, WhyLabs

## Recommended resources
- [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/)
- [MITRE ATLAS](https://atlas.mitre.org/)
- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- DEF CON AI Village content (free on YouTube)
- HackTheBox AI/ML challenges, AI Goat

## Recommended books / papers
- *Not with a Bug, But with a Sticker* — Ram Shankar Siva Kumar, Hyrum Anderson
- *The Developer's Playbook for Large Language Model Security* — Steve Wilson
- *Adversarial Machine Learning* — Anthony D. Joseph et al.
- NIST AI 100-2 (Adversarial ML taxonomy)

## Next step
Pick **one** specialization to start:

- Pentester background? → Try [Garak](https://github.com/NVIDIA/garak) on a local LLM and the OWASP LLM Top 10 labs.
- AppSec / Cloud background? → Build a RAG app yourself and intentionally introduce + then fix LLM vulnerabilities.
- GRC background? → Read NIST AI RMF cover-to-cover and map it to ISO 42001.
