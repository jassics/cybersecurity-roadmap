# Cloud Security Job Descriptions

This file contains representative Cloud Security JDs across **junior, mid, senior, and leadership** levels — based on real job postings from product companies, BigTech, BFSI, and consulting firms. They are paraphrased and de-identified.

Use them to:

- Understand what employers **actually expect** at each level
- Build / refine your resume to mirror the keywords
- Benchmark your current skills vs. target role

> Companion roadmap: [Cloud Security Career Roadmap](../cloud-security.md)

---

## 1. Cloud Security Analyst (Entry) — SaaS / Mid-size product company

**About the role**

You will be the first line of defense for our multi-account AWS environment, ensuring our cloud infrastructure remains secure, compliant, and aligned with industry best practices. You'll work closely with platform, DevOps, and SRE teams to triage misconfigurations and respond to cloud-native security alerts.

**Responsibilities**

- Monitor AWS Security Hub, GuardDuty, and CloudTrail-based detections; triage and escalate alerts
- Investigate and document misconfigurations identified by our CSPM tool (Wiz / Prisma Cloud)
- Maintain CIS AWS Foundations Benchmark compliance scores
- Support quarterly access reviews of IAM users, roles, and SSO assignments
- Help create runbooks and SOPs for common cloud incidents (public S3 bucket, IMDSv1 hosts, leaked keys)
- Assist with cloud-related portions of SOC 2 / ISO 27001 audits

**Required**

- 1–2 years in security operations or cloud engineering
- Working knowledge of AWS core services: IAM, S3, EC2, VPC, KMS, CloudTrail, CloudWatch
- Understanding of the Shared Responsibility Model
- Basic scripting in Python or Bash
- Familiarity with Linux, Git, and at least one ticketing system (Jira / ServiceNow)

**Nice to have**

- AWS Cloud Practitioner or AWS Security Specialty in progress
- Exposure to CSPM tools (Wiz, Prisma Cloud, Defender for Cloud)
- Experience writing Terraform or CloudFormation

---

## 2. Cloud Security Engineer (Mid) — Series B/C SaaS startup

**The role**

We're hiring a Cloud Security Engineer to own the security posture of our production AWS + Azure environments. You will work hand-in-hand with engineering to embed security into our cloud platform, not bolt it on.

**What you'll do**

- Design and implement preventive guardrails (AWS SCPs, Azure Policy, GCP Org Policies)
- Own our CNAPP (Wiz) — tune findings, build dashboards, drive remediation with engineering
- Build and maintain detections in AWS GuardDuty, Microsoft Sentinel, and our SIEM
- Lead cloud incident response (IAM compromise, leaked credentials, EBS/disk forensics)
- Improve our IaC pipeline security — Checkov / tfsec / KICS in CI; OPA / Conftest
- Manage cloud secrets lifecycle (AWS Secrets Manager, HashiCorp Vault, External Secrets Operator)
- Partner with the GRC team on SOC 2 Type II, ISO 27001, PCI-DSS evidence

**What you bring**

- 3–5 years working with cloud platforms in a security or platform role
- Deep knowledge of AWS IAM (policies, trust relationships, SCPs, permission boundaries) and at least one additional cloud
- Hands-on experience writing Terraform; reading other people's IaC fluently
- Strong Python or Go for automation
- Comfort with Kubernetes (EKS / AKS / GKE) — RBAC, NetworkPolicies, Pod Security Standards
- Experience with CSPM/CNAPP (Wiz, Prisma Cloud, Orca, Lacework, Defender for Cloud)
- Knowledge of MITRE ATT&CK Cloud Matrix
- Excellent written communication — you'll be writing RFCs and design docs

**Bonus**

- AWS Security Specialty, AZ-500, or GCP Professional Cloud Security Engineer
- Contributions to OSS cloud security tooling (Prowler, Cloud Custodian, Steampipe)
- Cloud incident response certifications (GIAC GCFA, GCDA)

---

## 3. Senior Cloud Security Engineer — BFSI / Bank

**Position summary**

The Senior Cloud Security Engineer leads the security architecture and engineering for the bank's regulated cloud workloads on AWS and Azure. The role partners with cloud platform engineering, risk, compliance, and audit teams to enforce regulatory commitments while accelerating safe cloud adoption.

**Key responsibilities**

- Design landing zone security baselines (AWS Control Tower / Azure Landing Zones) for multiple business units
- Architect cloud network security — VPC/VNet segmentation, Transit Gateway/vWAN, private endpoints, egress filtering
- Lead implementation of CIEM (Cloud Infrastructure Entitlement Management) — identify and remediate shadow admin paths
- Drive secure cloud-native logging strategy across CloudTrail, Config, CloudWatch, Activity Logs, and our SIEM
- Be the cloud security SME for RBI / regulator audit interactions
- Build threat models for new cloud-hosted products before they go live
- Mentor 3–4 junior and mid Cloud Security Engineers
- Evaluate CNAPP / cloud detection vendors (POCs, scoring matrices, exec presentations)

**Must have**

- 6–8 years in cloud security or cloud engineering, 4+ in security focus
- AWS Security Specialty AND Azure AZ-500 (or willingness to obtain within 6 months)
- Strong understanding of PCI-DSS 4.0, SOC 2, ISO 27001, and one of RBI Master Direction on IT / Cyber Security Framework, NIST 800-53, or FedRAMP
- Demonstrated experience writing complex Terraform modules used by multiple teams
- Strong Python; familiarity with Go
- Experience leading a cloud security incident end-to-end

**Soft skills**

- Ability to influence senior engineering leadership without authority
- Strong technical writing
- Comfortable presenting to regulators and external auditors

---

## 4. Cloud Security Architect — Global product organization

**Role overview**

As Cloud Security Architect, you will set the multi-cloud security architecture for our products serving 100M+ users worldwide. You'll be the most senior individual contributor in the Cloud Security function and will influence both engineering strategy and the broader Security org roadmap.

**You will**

- Define the multi-cloud (AWS, Azure, GCP) reference architectures: identity, networking, data, secrets, detection
- Lead M&A cloud security due diligence and integration playbooks
- Set the SCP / Org Policy / Azure Policy ruleset that 200+ engineering teams operate under
- Drive the strategy for consolidating CSPM + CWPP + CIEM + DSPM into one CNAPP platform
- Own the technical relationship with our top cloud security vendors
- Author and review RFCs that touch cloud security
- Represent the company externally — conference talks, OSS contributions, customer trust calls

**Required**

- 10+ years in security, with 6+ years specifically architecting cloud security solutions at scale
- Deep, demonstrable expertise in at least two of AWS / Azure / GCP at the architecture level
- Strong opinions, weakly held, on cloud-native vs third-party for CSPM, CWPP, secrets, IAM
- Experience leading **post-incident architecture changes** that prevented entire vulnerability classes
- Excellent communication — capable of moving exec opinion based on technical merit
- Track record of mentoring senior engineers

**Preferred**

- Experience operating in highly regulated environments (FedRAMP, PCI Level 1, HIPAA-covered)
- Public conference talks (re:Invent, RSAC, Black Hat, fwd:cloudsec)
- Open source maintainership of a notable cloud security project

---

## 5. Cloud Security Engineering Manager — Consulting firm

**Description**

We are looking for a Cloud Security Engineering Manager to lead a team of 6–10 consultants delivering cloud security assessments, transformation, and managed services for our enterprise clients across BFSI, retail, and tech.

**Responsibilities**

- Lead end-to-end delivery of cloud security engagements: assessment → roadmap → implementation → run
- Own utilization, quality, and CSAT for your team
- Hire, mentor, and develop a team of 6–10 cloud security engineers
- Be the deal-shaping technical lead for $500K+ engagements
- Build reusable accelerators (Terraform modules, playbooks, checklists)
- Stay hands-on enough to review complex client deliverables and escalate red flags

**Requirements**

- 10+ years total experience, with 5+ in cloud security
- 3+ years managing technical teams in a consulting / SI / Big 4 context
- Multiple cloud security certifications (AWS, Azure, or GCP — at least two)
- Demonstrated client-facing track record, including C-level communication
- Strong commercial acumen — SOW scoping, change orders, margin management

---

## What recruiters search for (keyword cheatsheet)

If you want to be found on LinkedIn / Naukri for Cloud Security roles, make sure your profile and resume include relevant terms below:

- **Platforms**: AWS, Azure, GCP, AWS Organizations, AWS Control Tower, Azure Landing Zones
- **Services**: IAM, KMS, Secrets Manager, CloudTrail, GuardDuty, Security Hub, Inspector, Macie, Config, Sentinel, Defender for Cloud, Security Command Center
- **Concepts**: Shared Responsibility, Zero Trust, Least Privilege, IMDSv2, SCP, Org Policy, CSPM, CWPP, CIEM, CNAPP, DSPM
- **IaC**: Terraform, CloudFormation, Pulumi, Bicep, Ansible
- **Containers**: EKS, AKS, GKE, Kubernetes RBAC, OPA, Kyverno
- **Standards**: CIS Benchmarks, SOC 2, ISO 27001, PCI-DSS, HIPAA, FedRAMP, NIST CSF, NIST 800-53, RBI cyber framework
- **Tools**: Wiz, Prisma Cloud, Lacework, Orca, Defender for Cloud, Snyk Cloud, Prowler, ScoutSuite, CloudSploit, Pacu, Stratus Red Team, Checkov, tfsec, KICS, Trivy
- **Certs**: AWS Security Specialty, AZ-500, GCP PCSE, CCSK, CCSP

---

> Have a great cloud security JD to add? PR welcome — see [Contribute.md](../Contribute.md).
