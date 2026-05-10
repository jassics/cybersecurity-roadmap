# DevSecOps Job Descriptions

This file contains representative DevSecOps JDs across **junior, mid, senior, and leadership** levels — paraphrased from real postings across SaaS, BigTech, BFSI, and consulting firms.

> Companion roadmap: [DevSecOps Career Roadmap](../devsecops.md)

---

## 1. Associate DevSecOps Engineer (Entry) — SaaS startup

**About the role**

We're looking for an Associate DevSecOps Engineer to help us integrate and operate security tools across our CI/CD pipelines. You'll work daily with engineering teams to ship secure code without slowing them down.

**What you'll do**

- Integrate and tune SAST (Semgrep, SonarQube), SCA (Dependabot, Snyk), secret scanning (gitleaks, trufflehog), and container scanning (Trivy) in GitHub Actions
- Triage and route findings to the right engineering teams in DefectDojo and Jira
- Help maintain pre-commit hooks and baseline security policies across repos
- Write small Python / Bash glue scripts that automate repetitive security work
- Document tooling and onboarding for engineering teams

**You should have**

- 1–2 years in DevOps, software engineering, or security operations
- Solid Git workflow knowledge (branches, PRs, code review)
- Hands-on with at least one CI system: GitHub Actions, GitLab CI, or Jenkins
- Familiarity with Docker, basic Kubernetes, and Linux
- Comfort writing simple Python or Bash scripts
- Awareness of OWASP Top 10 vulnerabilities

**Nice to have**

- AWS Cloud Practitioner / Azure Fundamentals
- Exposure to Terraform
- Started or finished CDP (Certified DevSecOps Professional) or similar

---

## 2. DevSecOps Engineer (Mid) — Series C product company

**The role**

As a DevSecOps Engineer on the Platform Security team, you'll design, build, and operate the security tools and guardrails that 150+ engineers use every day. You will own automation end-to-end, from problem statement to production rollout.

**Responsibilities**

- Own and continuously improve our CI/CD security pipeline (GitLab CI + Argo CD) — SAST, SCA, IaC scanning, container scanning, DAST baseline, secret scanning, SBOM generation (Syft, CycloneDX)
- Build policy-as-code with OPA / Rego, Conftest, and Kyverno for our Kubernetes platform
- Roll out artifact signing and verification using Sigstore (Cosign, Rekor, Fulcio)
- Build internal dashboards (Grafana / Snowflake) to track MTTR, scanner coverage, vuln age, and false positive rates
- Partner with AppSec to write custom Semgrep / CodeQL rules for org-specific vulnerability classes
- Run vulnerability management end-to-end in DefectDojo or your own tooling
- Manage secrets lifecycle (HashiCorp Vault, External Secrets Operator)
- Be on-call for the security platform (~1 week every 6–8 weeks)

**Requirements**

- 3–5 years in DevOps, SRE, or DevSecOps roles
- Strong Python or Go — you write tooling, not just configure it
- Deep CI/CD experience in at least one of GitHub Actions, GitLab CI, Jenkins, CircleCI
- Hands-on Kubernetes — building, debugging, securing
- Solid Terraform; able to write reusable modules
- Familiarity with OWASP Top 10 and Cloud Top 10
- Excellent communication — you'll need to PR-debate and influence engineers

**Bonus points**

- AWS / Azure / GCP Security certifications
- CKS (Certified Kubernetes Security Specialist)
- Contributions to open source security tooling
- Experience designing SLSA Level 2+ compliant builds

---

## 3. Senior DevSecOps Engineer — BFSI / Bank

**Position summary**

The Senior DevSecOps Engineer is responsible for shaping and operating the security platform that supports the bank's regulated cloud and on-prem workloads. You will partner with Engineering Excellence, Cloud Platform, Risk, and Internal Audit teams to embed security as code while satisfying regulatory commitments.

**Key responsibilities**

- Architect golden pipelines (Jenkins / GitHub Actions Enterprise) with mandatory security stages
- Own and continuously evolve the bank's policy-as-code framework (OPA, Rego, Sentinel)
- Drive software supply chain security strategy (SLSA Level 2 → Level 3, signed artifacts, restricted runners)
- Lead the rollout and operations of secrets management (HashiCorp Vault Enterprise)
- Define exception process and SLA for security findings; report MI to risk committees
- Mentor 3–5 DevSecOps engineers; participate in technical hiring
- Be the technical SME for RBI / regulator queries on the CI/CD and software supply chain

**Required**

- 6–9 years overall, 4+ years in DevSecOps / Platform Security at scale
- Expert-level CI/CD experience in a regulated environment
- Strong Python or Go, comfortable maintaining 500+ LOC services
- Multi-cloud security exposure (AWS + Azure at a minimum)
- Hands-on with HashiCorp Vault, Terraform Enterprise, Kubernetes
- Demonstrated experience designing or operating SLSA / SBOM / signing toolchains
- Familiarity with RBI Cyber Security Framework, ISO 27001, PCI-DSS, SOC 2

**Preferred**

- Public conference talks or OSS contributions
- CDP / CDE (Practical DevSecOps), CKS, AWS Security Specialty
- Experience leading post-incident DevSecOps platform improvements

---

## 4. Principal / Staff DevSecOps Engineer — BigTech / Product

**Role overview**

As Principal DevSecOps Engineer, you'll be the most senior individual contributor on the Engineering Security Platform team. You'll set the multi-year strategy for how thousands of engineers ship code securely.

**You will**

- Define the **paved roads / golden paths** for secure software delivery — the easy + fast + secure default
- Drive a multi-year supply chain security program (SLSA 3+, in-toto, hermetic builds, reproducible builds where applicable)
- Set the technical direction for our internal security platform: vuln management, scanners orchestration, policy engine, evidence store
- Influence vendor strategy across CNAPP, SCA, SAST, secrets vaults, and developer experience tools
- Own org-wide DevSecOps metrics that the CTO and CISO trust
- Coach Senior and Staff engineers; chair our DevSecOps architecture review board
- Represent the company externally — conference talks (e.g., SLSAcon, KubeCon, fwd:cloudsec), OSS leadership

**Required**

- 10+ years in engineering, with 5+ years architecting DevSecOps at scale (1000+ engineers OR 10000+ services)
- Track record of designing systems that other senior engineers want to use
- Deep expertise in at least two of: Kubernetes security, supply chain security, policy-as-code, secrets management, vulnerability orchestration
- Strong Go or Rust; comfortable contributing to open source security tooling
- Excellent technical writing — your RFCs are read by the CTO

**Preferred**

- Public technical reputation (talks, papers, OSS maintainership)
- Experience operating in highly regulated environments
- Contributions to standards bodies (SLSA, OpenSSF, CNCF SIG-Security)

---

## 5. DevSecOps Manager — Mid-size SaaS

**Description**

We are looking for a DevSecOps Manager to lead a team of 4–6 DevSecOps engineers responsible for the security tooling, CI/CD security, and developer experience for our 200+ engineers.

**Responsibilities**

- Hire, mentor, and develop a team of 4–6 DevSecOps engineers
- Own the team's roadmap, OKRs, and quarterly review cycles
- Partner with Engineering, AppSec, Cloud Security, and GRC leaders on cross-functional initiatives
- Be the budget owner for DevSecOps tooling
- Be hands-on enough to review PRs, design docs, and join customer security calls
- Be the internal advocate for engineering productivity AND security — the two must coexist

**Requirements**

- 8+ years total, with 3+ years managing technical security or platform teams
- Strong technical depth — you don't need to be the best coder on your team, but you must earn their trust
- Proven track record building DevSecOps programs from scratch or scaling them 3–10x
- Excellent stakeholder management
- Strong written and verbal communication

---

## What recruiters search for (keyword cheatsheet)

- **CI/CD**: GitHub Actions, GitLab CI, Jenkins, CircleCI, Buildkite, Tekton, Argo CD, Spinnaker
- **SAST / SCA / DAST**: Semgrep, CodeQL, SonarQube, Snyk, Checkmarx, Veracode, Fortify, Dependabot, Renovate, OWASP Dependency-Check, OWASP ZAP, Burp Suite Enterprise, Nuclei
- **Container**: Trivy, Grype, Docker Scout, Clair, Anchore, Aqua
- **IaC**: Checkov, tfsec, KICS, Terrascan, Snyk IaC
- **Secrets**: gitleaks, trufflehog, HashiCorp Vault, AWS Secrets Manager, External Secrets Operator
- **Policy**: OPA, Rego, Conftest, Kyverno, Gatekeeper, Sentinel, Cloud Custodian
- **Supply chain**: SLSA, in-toto, Cosign, Rekor, Fulcio, Syft, CycloneDX, SPDX, GUAC
- **Languages**: Python, Go, Bash, sometimes Rust / Java / TypeScript
- **Platforms**: Kubernetes, EKS, AKS, GKE, OpenShift, Linux, Docker
- **Standards**: NIST SSDF, OWASP DSOMM, BSIMM, SLSA, SOC 2, ISO 27001
- **Certs**: CDP, CDE, CKS, AWS Security Specialty, AZ-500

---

## What good DevSecOps interviews look like

Most companies will test you on a combination of:

1. **Hands-on coding** — write a small script that scans a repo / parses a SARIF / Trivy output / SBOM
2. **CI/CD design** — draw a pipeline that includes SAST, SCA, IaC, container, DAST, SBOM, signing; defend your choices
3. **Policy design** — write an OPA/Rego rule for a Terraform / Kubernetes resource
4. **Vulnerability triage** — given a SCA report with 500 findings, how do you prioritize?
5. **Behavioral** — how do you partner with engineering when they push back on security gates?

---

> Have a DevSecOps JD to add? PR welcome — see [Contribute.md](../Contribute.md).
