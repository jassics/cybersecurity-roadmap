# AI / ML Security Job Descriptions

Representative JDs from product companies, BigTech, AI labs, BFSI, and consulting firms for **AI / ML / GenAI Security** roles. Paraphrased and de-identified.

> Companion roadmap: [AI / ML Security Career Roadmap](../ai-security-career-roadmap.md) \u00b7 [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

---

## 1. AI Security Analyst (Entry) \u2014 GenAI-heavy SaaS

**About the role**

We're hiring an AI Security Analyst to help us secure the GenAI features shipped across our product. You will work with ML, product, and platform security teams to identify, triage, and remediate AI-specific risks.

**Responsibilities**

- Triage prompt injection, jailbreak, and abuse reports from our customers and bug bounty program
- Review LLM features and AI agent workflows against the **OWASP Top 10 for LLM Applications** and **MITRE ATLAS**
- Maintain and tune LLM guardrails (NeMo Guardrails / Guardrails AI / LLM-Guard / custom)
- Run red-team exercises against new AI features before launch
- Help document responsible AI principles and internal usage policies
- Stay current with adversarial ML and LLM attack research

**Required**

- 1\u20132 years in security engineering, AppSec, or ML engineering
- Strong Python; comfort with REST APIs, JSON, prompt design
- Understanding of LLM fundamentals \u2014 tokens, context windows, system prompts, RAG, function calling
- Familiarity with OWASP LLM Top 10, MITRE ATLAS
- Solid web/API security basics (OWASP Top 10)

**Nice to have**

- Prior CTF / bug bounty work focused on LLMs
- Exposure to LangChain, LlamaIndex, AutoGen, CrewAI
- AWS Bedrock, Azure OpenAI, or GCP Vertex AI hands-on

---

## 2. AI / LLM Red Team Engineer (Mid) \u2014 Frontier AI lab

**The mission**

You will join the AI Red Team responsible for finding novel attacks against our flagship multimodal model and the agents built on top of it.

**What you'll do**

- Run structured red-team campaigns across text, image, audio, and tool-use modalities
- Discover and document novel prompt-injection, jailbreak, and chain-of-thought leakage techniques
- Build internal tooling and automation around `Garak`, `PyRIT`, `Promptfoo`, `DeepEval`, custom harnesses
- Partner with policy and alignment teams to define harm taxonomies
- Influence model post-training (RLHF, RLAIF, constitutional AI) based on findings
- Author internal write-ups; contribute to public model / system cards

**What we want**

- 3\u20135 years in offensive security, AppSec, or ML research
- Demonstrated track record of public LLM-focused research, CTFs, or bug bounty (or willingness to share past private work under NDA)
- Strong Python; comfortable with PyTorch / transformers / Hugging Face
- Deep understanding of LLM internals (attention, tokenization, sampling, alignment techniques)
- Excellent technical writing

**Bonus**

- Background in linguistics, cognitive science, or formal verification
- Published research at NeurIPS, ICLR, USENIX Security, IEEE S&P
- Contributions to OSS AI security tools

---

## 3. ML / AI Security Engineer (Mid) \u2014 Cloud platform company

**Position summary**

You will own the security of the ML/AI platform that our internal data science teams and external customers use to train, deploy, and serve models on our cloud.

**Key responsibilities**

- Threat-model ML pipelines end-to-end \u2014 ingest, train, store, serve, monitor
- Secure model artifacts (signing, attestation, registry RBAC, ModelScan / Protect AI)
- Build LLM gateway controls \u2014 prompt logging, PII redaction, rate limiting, content filters, output validation
- Harden MLOps services \u2014 Kubeflow, MLflow, SageMaker, Vertex AI, Bedrock; tighten IAM and network access
- Defend against adversarial ML attacks \u2014 evasion, poisoning, membership inference, model extraction
- Run internal red-team exercises; partner with product security for feature reviews
- Drive evidence collection for SOC 2 / ISO 27001 / **ISO/IEC 42001** AI controls

**Must have**

- 3\u20136 years total, with 2+ years in security and exposure to ML/MLOps
- Strong cloud security skills in at least one of AWS / Azure / GCP
- Python; comfortable reading PyTorch / TF / JAX code
- Hands-on with at least one ML platform (SageMaker / Vertex / Databricks / Azure ML)
- Knowledge of OWASP LLM Top 10, MITRE ATLAS, NIST AI RMF
- Familiarity with Kubernetes, Docker, IaC (Terraform)

**Preferred**

- Cloud security cert (AWS Security Specialty, AZ-500, GCP PCSE)
- AI/ML cert (AWS ML Specialty, Azure AI Engineer)
- [CAISP: Certified AI Security Professional](https://www.practical-devsecops.com/certified-ai-security-professional/?fpr=jassics)

---

## 4. Senior AI Security Engineer \u2014 BFSI / Bank

**About the team**

The bank is integrating GenAI into customer support, fraud detection, KYC, and developer productivity. The Senior AI Security Engineer will set and enforce the security and governance bar for AI adoption.

**Responsibilities**

- Architect the bank's central **LLM gateway** (centralized auth, logging, content filtering, DLP)
- Define AI usage policies and acceptable-use guardrails for 10,000+ employees
- Threat-model every customer-facing or fraud-affecting AI feature
- Manage third-party AI model and SaaS risk (OpenAI, Anthropic, Google, Microsoft, niche vendors)
- Be the SME for regulator queries (RBI / SEBI / EBA-DORA equivalents) on AI risk
- Drive **ISO/IEC 42001** AI management system implementation
- Mentor 2\u20133 junior engineers; participate in technical hiring

**Required**

- 6\u20139 years in security, with at least 2\u20133 years focused on AI/ML
- Working knowledge of: NIST AI RMF, EU AI Act, ISO 42001, India DPDP Act + emerging AI rules
- Strong cloud security (AWS / Azure / GCP), at least one cert
- Comfortable reading ML / LLM code
- Excellent written + verbal communication

**Preferred**

- Public talks or blog posts on AI security
- Experience running an AI red team or AI bug bounty program

---

## 5. Principal AI Security Engineer / AI Security Architect \u2014 BigTech

**Role overview**

The Principal AI Security Engineer is the most senior IC for AI security in our engineering org. You will set the multi-year strategy for how we ship AI products safely at planetary scale.

**You will**

- Define the reference architecture for **secure agentic systems** \u2014 tool authorization, sandboxing, supervision
- Lead industry-shaping research: novel attacks, novel defenses, model attestation, AI bill of materials (AI-BOM)
- Set the AI red team's strategic roadmap; influence model post-training
- Influence cross-org vendor strategy across model providers, eval frameworks, guardrails
- Represent the company in standards bodies (NIST, ISO/IEC JTC 1 SC 42, OWASP, MLCommons)
- Coach Senior and Staff engineers across multiple AI product teams
- Engage with regulators, customers, and the board on AI risk

**Required**

- 10+ years in security, with 4\u20136 years deeply in AI/ML security
- Public technical reputation (papers, talks, OSS) in AI security
- Deep understanding of LLM architecture, alignment, agent frameworks, and adversarial ML
- Strong systems design background; comfortable designing distributed systems
- Excellent technical writing; your RFCs are read by the CTO

**Preferred**

- Contributions to OWASP LLM Top 10, MITRE ATLAS, NIST AI RMF, or similar
- Active maintainership of an AI security OSS project

---

## 6. AI Governance / Responsible AI Analyst \u2014 Consulting / GRC track

**Description**

You will help our enterprise clients build AI governance programs aligned with global regulations and internal risk appetite.

**Responsibilities**

- Conduct AI risk assessments using NIST AI RMF and ISO 42001 controls
- Author AI policies, acceptable-use guidelines, and DPIAs covering generative AI
- Maintain inventories of AI systems (in-house + third-party) and their risk classifications
- Map use cases to regulatory regimes (EU AI Act risk tiers, India DPDP, sector-specific rules)
- Run AI bias / fairness / explainability assessments
- Train executive and engineering teams on responsible AI

**Required**

- 3\u20135 years in GRC, privacy, or risk consulting
- Familiarity with NIST AI RMF, ISO/IEC 42001, OECD AI Principles
- One of CIPP/E, CIPM, CIPT (IAPP)
- Strong written communication and stakeholder management
- Comfort reading technical documentation about ML systems (no coding required)

**Preferred**

- Legal or audit background
- [CAISP](https://www.practical-devsecops.com/certified-ai-security-professional/?fpr=jassics) or similar AI security cert

---

## What recruiters search for (keyword cheatsheet)

- **Standards**: OWASP LLM Top 10, MITRE ATLAS, NIST AI RMF (AI 600-1), ISO/IEC 42001, ISO/IEC 23894, EU AI Act, India DPDP, OECD AI Principles
- **Models / runtimes**: GPT-4 / 4o / 5, Claude 3.5/4, Gemini 1.5/2, Llama 3/4, Mistral, Qwen, DeepSeek
- **Frameworks**: LangChain, LangGraph, LlamaIndex, AutoGen, CrewAI, Semantic Kernel, Haystack
- **MLOps**: SageMaker, Vertex AI, Bedrock, Azure OpenAI, MLflow, Kubeflow, Triton, Ray Serve
- **Red team / eval**: Garak, PyRIT, Promptfoo, DeepEval, llm-attacks, AdvBench, HarmBench
- **Guardrails**: NeMo Guardrails, Guardrails AI, LLM-Guard, Rebuff, Llama Guard, Azure AI Content Safety
- **Model security**: ModelScan, Protect AI, HiddenLayer, AI-BOM, Sigstore for models
- **Adversarial ML**: ART (Adversarial Robustness Toolbox), CleverHans, Foolbox
- **Vector DBs**: pgvector, Pinecone, Weaviate, Chroma, Qdrant, Milvus
- **Concepts**: prompt injection (direct / indirect / multimodal), jailbreak, RAG poisoning, data exfiltration, model inversion, membership inference, model extraction, training data poisoning, supply-chain attacks on weights

---

> Have an AI Security JD to add? PR welcome \u2014 see [Contribute.md](../Contribute.md).
