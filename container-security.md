# Container & Kubernetes Security Career Roadmap

> 📘 Recommended study plans: [Secure Software Development Lifecycle](https://github.com/jassics/security-study-plan/blob/main/secure-software-development-lifecycle-study-plan.md) · [Product Security](https://github.com/jassics/security-study-plan/blob/main/product-security-study-plan.md) · [Common Skills](https://github.com/jassics/security-study-plan/blob/main/common-skills-study-plan.md).

Container Security is a **specialization** rather than a starting domain. People rarely start their career here directly — most enter via DevSecOps, Cloud Security, or SRE backgrounds. But once you're in, demand is high and salaries are competitive.

## Who is this for?
- DevSecOps / Cloud engineers wanting deeper container expertise
- SRE / Platform engineers shifting toward security
- AppSec engineers handling containerized microservices

## Pre-requisites (foundation)
1. Linux internals — namespaces, cgroups, capabilities, seccomp, AppArmor/SELinux
2. Docker fundamentals — image layers, Dockerfile, registries, networking
3. Kubernetes core — Pods, Deployments, Services, RBAC, Namespaces, NetworkPolicy
4. CI/CD basics
5. At least one cloud provider's managed K8s (EKS / AKS / GKE)
6. YAML, shell, basic Go (helpful for K8s ecosystem)

## Career ladder

### Entry level (0–2 years in container security; rarely a first job)
**Typical entry routes:**

- Junior DevSecOps / Cloud Security Analyst handling container findings
- Associate Container Security Engineer (rare; usually in product companies)

**Skills to focus on:**

1. **Container image security** — minimal base images (distroless, alpine), multi-stage builds
2. **Image scanning** — Trivy, Grype, Snyk Container, Docker Scout, Clair
3. **Dockerfile best practices** — non-root user, COPY vs ADD, layer caching, secrets handling
4. **Registry security** — private registries, signing (Cosign, Notary v2)
5. **CIS Docker Benchmark + CIS Kubernetes Benchmark**
6. **Kubernetes RBAC** — Roles, ClusterRoles, ServiceAccounts
7. **Pod Security Standards** (Privileged / Baseline / Restricted)
8. **NetworkPolicy** basics — default deny, allow-only patterns

### Mid level (2–5 years)
**Possible job titles:**

- Container Security Engineer
- Kubernetes Security Engineer
- Cloud-Native Security Engineer
- DevSecOps Engineer (containers focus)

**New skills to add:**

1. **Admission control** — OPA Gatekeeper, Kyverno, Validating/Mutating Admission Webhooks
2. **Runtime security** — Falco, Tetragon (eBPF), Tracee, Sysdig Secure
3. **Service Mesh security** — Istio / Linkerd mTLS, authorization policies
4. **Supply chain security** — SBOM (Syft), SLSA framework, Sigstore (Cosign, Rekor, Fulcio)
5. **Secrets management** — Sealed Secrets, External Secrets Operator, Vault Agent Injector
6. **Multi-tenant K8s security** — namespace isolation, vCluster, Capsule
7. **Kubernetes pentest basics** — kube-hunter, kubectl-who-can, peirates
8. **GitOps security** — ArgoCD / Flux RBAC, drift detection

**Certs to consider:**

- CKA → CKS (Certified Kubernetes Security Specialist) — the must-have
- [CCSE](https://www.practical-devsecops.com/certified-container-security-expert/?fpr=jassics)
- [CCNSE](https://www.practical-devsecops.com/certified-cloud-native-security-expert/?fpr=jassics)

### Senior level (5–8 years)
**Possible job titles:**

- Senior Container Security Engineer
- Lead Cloud-Native Security Engineer
- Kubernetes Security Tech Lead

**New focus areas:**

1. **Multi-cluster / multi-cloud K8s security architecture**
2. **eBPF-based security tooling** design
3. **Threat modeling K8s clusters**
4. **Incident response for compromised clusters** (etcd forensics, audit logs)
5. **Custom admission controllers** in Go
6. **Building secure base images and golden paths** for engineering teams
7. **PCI / HIPAA in Kubernetes** — segmentation, compliance evidence

### Staff / Principal / Architect (8+ years)
**Possible job titles:**

- Principal Cloud-Native Security Engineer
- Container / K8s Security Architect
- Head of Cloud-Native Security

**Focus areas:**

- Cloud-native security strategy across business units
- Influencing CNCF tool selection and platform direction
- Building security platform teams
- Industry contributions — talks, OSS, CNCF SIGs

## Career paths from Container Security

```text
                  Container Security
                          │
       ┌──────────────────┼──────────────────┐
       ▼                  ▼                  ▼
   DevSecOps          Cloud Security      Platform Sec
   (CI/CD focus)      (multi-cloud)       Engineer (SRE+)
       │                  │                  │
       ▼                  ▼                  ▼
   Supply Chain      Cloud Security     Distinguished
   Security Lead     Architect          Platform Engineer
                          │
                          ▼
                  Enterprise Security Architect
```

## Lateral pivots from Container Security
- **→ Cloud Security** — natural extension; container security IS cloud-native security
- **→ DevSecOps** — broader pipeline ownership
- **→ Supply Chain Security** — SLSA, SBOM, signing focus
- **→ Platform Engineering** — internal developer platforms with security baked in
- **→ Kubernetes Pentester / Red Team** — offensive specialization

## Recommended tools to master
- **Scanning**: Trivy, Grype, Snyk, Docker Scout, Clair
- **Policy**: OPA / Gatekeeper, Kyverno, Polaris
- **Runtime**: Falco, Tetragon, Tracee, Sysdig
- **Supply chain**: Cosign, Syft, in-toto, SLSA
- **Pentest**: kube-bench, kube-hunter, peirates, kubectl-who-can

## AI-augmented Container & K8s Security (you need this in 2025+)
AI is moving fast in the cloud-native ecosystem — both in tooling and in workloads.

### Using AI to do K8s security better
1. **AI-assisted YAML review** — prompt LLMs to find missing `securityContext`, `runAsNonRoot`, `readOnlyRootFilesystem`, NetworkPolicy gaps
2. **OPA / Kyverno policy generation** — first-draft policies from natural-language requirements
3. **CVE → fix suggestions** for container scan output (Trivy / Grype)
4. **`kubectl` natural language** — K8sGPT, kubectl-ai for cluster queries and diagnostics
5. **Falco / Tetragon rule authoring** with AI assistance

### Securing AI workloads on Kubernetes
Most production AI now runs on K8s (KServe, Kubeflow, Ray, vLLM, TGI):

1. **GPU security** — GPU operator privileges, MIG isolation, GPU driver CVEs
2. **Inference server hardening** — KServe / Triton / vLLM / TGI exposure; auth on inference endpoints
3. **Model storage in pods** — PV / PVC for model weights; OCI-image-backed models (ORAS, ModelKit)
4. **MLOps pipeline RBAC** — Kubeflow Pipelines / Argo Workflows running with privileged service accounts is the common path to compromise
5. **Multi-tenant inference** — namespace isolation, resource quotas, network policies between tenants
6. **Egress from inference pods** — prevent data exfil via outbound calls from agents
7. **Sigstore / Cosign for models** — sign and verify model artifacts in admission control

See: [AI Security Career Roadmap](ai-security-career-roadmap.md) · [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

## Recommended labs / resources
- Kubernetes Goat
- KubeCon talks (CNCF YouTube)
- Killer.sh CKS simulator
- Kube-stride (threat modeling K8s)

## Recommended books
- *Kubernetes Security and Observability* — Brendan Creane, Amit Gupta
- *Container Security* — Liz Rice
- *Hacking Kubernetes* — Andrew Martin, Michael Hausenblas

## Next step
If you don't already have Kubernetes daily-driver experience, start with CKA → CKS. Then deploy Kubernetes Goat and break it for a week.
