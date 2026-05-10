# Cloud Security Skills and Career Roadmap

> 📘 Recommended study plans: [Common Skills](https://github.com/jassics/security-study-plan/blob/main/common-skills-study-plan.md) · [Product Security](https://github.com/jassics/security-study-plan/blob/main/product-security-study-plan.md) · [IAM Security](https://github.com/jassics/security-study-plan/blob/main/iam-security-study-plan.md).

Cloud Security is the **fastest growing** specialization in cybersecurity. Almost every organization is moving workloads to AWS / Azure / GCP and they all need engineers who can secure them.

> Assumption: You are comfortable with Cloud Computing fundamentals (service vs. deployment models, IaaS/PaaS/SaaS) and have hands-on with at least **one** Cloud Service Provider. If not, finish [common-skills.md](common-skills.md) → Cloud Computing Fundamentals first.

## Who is this for?
- Cloud engineers / SREs / DevOps engineers pivoting into security
- AppSec / NetSec engineers expanding into cloud
- Sysadmins moving from on-prem to cloud-native security

## Pre-requisites (foundation)
1. Pick **one cloud provider deep** (AWS recommended for jobs market) — services, regions, IAM
2. Linux + scripting (Bash, Python)
3. Networking basics — VPC, subnets, routing, security groups
4. Git + at least one IaC tool (Terraform preferred)
5. Containers & Kubernetes basics
6. CI/CD basics (GitHub Actions / GitLab CI / Jenkins)
7. Understanding of the **Shared Responsibility Model**

## Career ladder

### Entry level (0–2 years)
**Possible job titles:**

- Cloud Security Analyst
- Junior Cloud Security Engineer
- Cloud SOC Analyst
- Associate Cloud Security Consultant

**Skills to focus on:**

1. **IAM deep dive** (per cloud) — users, roles, policies, trust relationships, least privilege
2. **AWS core security services**: IAM, S3 (bucket policies, encryption, public access), KMS, CloudTrail, CloudWatch, Security Hub, GuardDuty, Inspector, Config
3. **Azure core**: Entra ID (Azure AD), Defender for Cloud, Sentinel, Key Vault, Storage security
4. **GCP core**: IAM, Cloud Audit Logs, Security Command Center, KMS, Org Policies
5. **CIS Benchmarks** for your cloud
6. **Reading cloud logs** — CloudTrail / Activity Log / Audit Log analysis
7. **Common misconfigs** — public S3, open security groups, overprivileged roles, unencrypted disks
8. **Hands-on labs** — flaws.cloud, flaws2.cloud, CloudGoat, Azure Goat, GCP Goat

**Entry certs:**

- AWS Cloud Practitioner → AWS Security Specialty (SCS-C02)
- AZ-900 → AZ-500 (Azure Security Engineer)
- Google Cloud Digital Leader → Professional Cloud Security Engineer
- CCSK (vendor-neutral) — great starter

### Mid level (2–5 years)
**Possible job titles:**

- Cloud Security Engineer
- CSPM / CNAPP Engineer
- Cloud Detection & Response Engineer
- DevSecOps Engineer (cloud-heavy)

**New skills to add:**

1. **CSPM / CNAPP tools** — Wiz, Prisma Cloud, Orca, Lacework, Defender CSPM
2. **CWPP** — workload protection for VMs / containers / serverless
3. **CIEM** — cloud entitlement management; finding shadow admins
4. **Multi-cloud basics** — second cloud at working level
5. **Infrastructure as Code security** — Terraform + Checkov / tfsec / KICS / Trivy
6. **Container & Kubernetes security** (see [container-security.md](container-security.md))
7. **Serverless security** — Lambda / Azure Functions / Cloud Run permissions, layers
8. **Threat detection** — writing GuardDuty / Sentinel / SCC rules; understanding MITRE ATT&CK Cloud Matrix
9. **Cloud incident response** — IR playbooks, EBS/disk forensics, log preservation
10. **Cloud pentesting basics** — AWS metadata abuse, IAM privilege escalation, SSRF→cloud

**Certs to consider:**

- AWS Security Specialty
- Azure AZ-500
- GCP Professional Cloud Security Engineer
- CCSP (broader management-tilted)
- CCSK Plus

### Senior level (5–8 years)
**Possible job titles:**

- Senior Cloud Security Engineer
- Lead Cloud Security Engineer
- Cloud Security Tech Lead
- Senior Cloud DevSecOps Engineer

**New focus areas:**

1. **Multi-cloud / hybrid cloud security strategy**
2. **Landing Zone design** — AWS Control Tower / Azure Landing Zones / GCP Org setup
3. **SCP / Org Policy** design at scale
4. **Cloud incident response leadership**
5. **Cost-aware security** — picking tools that scale economically
6. **Compliance mapping** — SOC 2, ISO 27017/27018, PCI-DSS in cloud, FedRAMP
7. **Threat modeling cloud architectures**
8. **Building security guardrails** in pipelines (policy-as-code with OPA, Cloud Custodian)

### Staff / Principal / Architect (8+ years)
**Possible job titles:**

- Cloud Security Architect
- Principal Cloud Security Engineer
- Head of Cloud Security
- Multi-Cloud Security Architect

**Focus areas:**

- Org-wide cloud security strategy and reference architectures
- M&A cloud security due diligence
- Vendor consolidation (CSPM + CWPP + CIEM → CNAPP)
- Influencing platform/eng decisions; chairing arch review boards
- Talent strategy, hiring, building Cloud SecEng teams

## Career paths from Cloud Security

```text
                    Cloud Security (entry)
                              │
       ┌──────────────┬───────┴───────┬──────────────┐
       ▼              ▼               ▼              ▼
   CSPM / CNAPP    Cloud DevSecOps   Cloud SOC /    Cloud
   Engineer        Engineer          Detection      Pentester
       │              │               │              │
       ▼              ▼               ▼              ▼
   Cloud IAM     Platform Sec     Threat Hunter   Red Team
   Architect     Engineer         (Cloud)         (Cloud)
       │
       ▼
  Cloud Security Architect ──► Multi-Cloud / Enterprise Architect
```

## Lateral pivots from Cloud Security
- **→ DevSecOps** — same toolchain, more pipeline focus
- **→ Container / Kubernetes Security** — natural deepening
- **→ Application Security** — secure the apps running in the cloud you protect
- **→ GRC / Compliance Engineering** — automate SOC 2 / ISO controls
- **→ Cloud SRE / Platform Engineering** — reliability + security hybrid

## Recommended tools to learn
- **IaC scanning**: Checkov, tfsec, KICS, Terrascan, Trivy
- **CSPM/CNAPP**: Wiz, Prisma Cloud, Orca, Lacework, Defender for Cloud, Snyk Cloud
- **Cloud pentest**: Pacu (AWS), ScoutSuite, Prowler, CloudSploit, MicroBurst (Azure)
- **Detection**: GuardDuty, Security Hub, Sentinel, Chronicle, Falco, CloudQuery
- **Policy as code**: OPA / Rego, Cloud Custodian, AWS SCPs, Azure Policy, GCP Org Policy

## AI-augmented Cloud Security (you need this in 2025+)
AI is reshaping both how we work and what we secure in the cloud.

### Using AI to do cloud security better
1. **AI assistants for IaC review** — use Copilot Chat / Cursor / Claude Code to find IAM permission issues, public S3 buckets, missing encryption in Terraform / CloudFormation
2. **AI-assisted IAM analysis** — paste large policies, trust relationships, or access-analyzer findings and ask for permission boundaries
3. **AI-driven log triage** — ask an LLM to explain a CloudTrail event chain or a GuardDuty finding in business language
4. **Cloud query generation** — prompt for SPL / KQL / Steampipe SQL queries to hunt for misconfigurations
5. **Architecture diagrams** — use AI to convert prose runbooks into Mermaid / draw.io for design reviews

### Securing AI workloads in the cloud
Every cloud now runs AI — Bedrock, Vertex AI, Azure OpenAI, SageMaker, hosted Hugging Face. You'll be asked to secure these.

1. **AI service IAM** — least-privilege for Bedrock / Vertex / OpenAI roles; deny `*Invoke*` from unintended principals
2. **Private connectivity** — PrivateLink / Private Endpoint for AI APIs; no traffic to public internet
3. **Prompt / completion logging strategy** — logs contain PII; design retention + access controls
4. **Model & dataset storage** — S3 / GCS / ADLS classification, KMS, signed model artifacts, ModelScan / Protect AI
5. **Egress controls for agents** — AI agents need network policy: which APIs can they hit?
6. **Cost-based DoS** — LLM token usage as billable resource; abuse can hit thousands of dollars per hour
7. **Service-to-service auth** — STS / workload identity / managed identity for AI services
8. **Compliance** — ISO/IEC 42001, NIST AI RMF mapped to cloud controls

See: [AI Security Career Roadmap](ai-security-career-roadmap.md) · [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

## Recommended labs / courses
- flaws.cloud, flaws2.cloud (free, classic)
- CloudGoat (Rhino Security Labs)
- AzureGoat, GCP Goat
- Cybr.com cloud labs
- AWS Skill Builder, Microsoft Learn (free)

## Recommended books
- *AWS Security* — Dylan Shields
- *Practical Cloud Security* — Chris Dotson
- *Hacking the Cloud* — Nick Frichette (free online resource)

## Next step
Pick **one** cloud, do flaws.cloud + CloudGoat, then attempt AWS Security Specialty or AZ-500. Don't try to learn all three clouds simultaneously — depth first, breadth later.
