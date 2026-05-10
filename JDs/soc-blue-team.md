# SOC / Blue Team Job Descriptions

Representative SOC Analyst, Incident Responder, Threat Hunter, Detection Engineer, and DFIR JDs.

> Companion roadmap: [SOC / Blue Team Career Roadmap](../soc-blue-team.md) \u00b7 [Blue Team Study Plan](https://github.com/jassics/security-study-plan/blob/main/blue-team-detection-response-study-plan.md)

---

## 1. SOC Analyst L1 (Entry) \u2014 24x7 MSSP

**About the role**

You will be on the front line of our 24x7 SOC, monitoring our customer environments and triaging alerts before they reach our L2 / L3 teams.

**Responsibilities**

- Monitor SIEM (Splunk, Sentinel, Chronicle, or Elastic) dashboards across customer tenants
- Triage alerts as true positive / false positive / benign true positive
- Enrich indicators using VirusTotal, AbuseIPDB, GreyNoise, URLScan, any.run
- Escalate confirmed incidents to L2 with a complete handover note
- Follow runbooks for known incident types (phishing, brute force, malware, suspicious login)
- Maintain ticket hygiene; meet SLA targets

**Required**

- 0\u20132 years in IT / security
- Strong understanding of TCP/IP, DNS, HTTP, common ports
- Familiarity with Windows + Linux command line
- Awareness of MITRE ATT&CK at a basic level
- Strong written English; willing to work in shifts
- Comfort with one ticketing system

**Nice to have**

- CompTIA Security+, CySA+, or Blue Team Level 1 (BTL1)
- Splunk Core Certified User or Microsoft SC-200
- Home lab / TryHackMe / LetsDefend / BTLO experience

---

## 2. SOC Analyst L2 / Incident Responder (Mid) \u2014 Product company

**Position summary**

L2 owns deeper investigations escalated from L1. You will pivot across endpoint, network, identity, and cloud data sources to determine scope and impact.

**Responsibilities**

- Lead investigations across EDR (CrowdStrike / SentinelOne / Defender), SIEM, NDR, and cloud audit logs
- Build timelines of attacker activity
- Contain incidents \u2014 host isolation, credential reset, IAM revocation
- Drive eradication and recovery with engineering and IT teams
- Write incident reports and lessons-learned briefings
- Tune detection rules to reduce false positives
- Be part of an on-call rotation

**Required**

- 2\u20135 years in SOC / IR / security operations
- Strong SIEM query skills in one of Splunk SPL, KQL, Chronicle YARA-L, Elastic ESQL
- EDR fluency \u2014 deep familiarity with at least one major vendor
- Working knowledge of MITRE ATT&CK
- Understanding of Windows + Active Directory attacks (Kerberoasting, PtH, lateral movement)
- Python or PowerShell scripting

**Bonus**

- GIAC GCIH, GCIA, Blue Team Level 2 (BTL2)
- Cloud incident response experience (AWS / Azure / GCP)
- Memory forensics with Volatility / MemProcFS

---

## 3. Senior Threat Hunter \u2014 Tech enterprise

**The role**

You will run a hypothesis-driven threat hunting program against our 100,000+ endpoint environment and multi-cloud footprint.

**Responsibilities**

- Develop and execute threat hunts based on MITRE ATT&CK coverage gaps and threat intel
- Build hunt notebooks in Jupyter / msticpy / Hunting ELK
- Convert successful hunts into long-running detections (Sigma, KQL, Splunk ESCU)
- Partner with the red team and purple team to validate detection coverage
- Stay current with adversary TTPs (DFIR Report, MISP, Mandiant, Microsoft Threat Intel)
- Coach L1 / L2 analysts; mentor junior hunters

**Required**

- 5\u20138 years in SOC, IR, or threat hunting
- Deep MITRE ATT&CK knowledge across Enterprise + Cloud matrices
- Strong scripting (Python preferred)
- Demonstrable hunt-to-detection track record
- Experience writing and reviewing Sigma rules
- Excellent written communication

**Preferred**

- SANS FOR508 / FOR578 / GCTI / GCFA
- Public talks or write-ups on threat hunting
- Active in OSS detection projects (Sigma, Elastic Detection Rules, Sentinel rules)

---

## 4. Detection Engineering Lead \u2014 Product company

**Description**

You will lead the Detection Engineering function for our security platform team. You'll treat detections like code \u2014 versioned, tested, deployed via CI \u2014 and own coverage across endpoint, cloud, identity, and SaaS.

**Responsibilities**

- Set the strategy for detection-as-code at the company
- Build and maintain the detection content pipeline (git repo \u2192 CI tests \u2192 SIEM / EDR deploy)
- Define detection KPIs (TP/FP rate, MTTD, coverage by ATT&CK technique)
- Lead vendor evaluation for SIEM / SOAR / NDR
- Drive cross-team purple team exercises
- Build a team of 3\u20136 Detection Engineers

**Required**

- 6\u20139 years in blue team roles
- Track record of leading or building a detection-as-code program
- Strong Python or Go
- Experience with at least one SIEM at scale (Splunk, Sentinel, Chronicle, Elastic)
- Knowledge of ATT&CK, Sigma, YARA, OSQuery
- Hiring + mentoring experience

**Preferred**

- GIAC GCDA / GCFA / GREM
- Active open source contributions
- Cloud security expertise

---

## 5. Senior DFIR Consultant \u2014 IR firm / Big 4

**Role overview**

You will lead high-impact incident response engagements at client sites \u2014 ransomware, business email compromise, nation-state intrusions, insider threats.

**Responsibilities**

- Lead client IR engagements from triage through to remediation and final report
- Collect, preserve, and analyze digital evidence (disk, memory, cloud, network)
- Run forensic timeline reconstructions across Windows / Linux / macOS / cloud
- Interface with clients' executives, counsel, insurers, and (when relevant) law enforcement
- Mentor junior DFIR consultants on case work
- Contribute to internal threat intelligence and methodology improvements

**Required**

- 7\u201310+ years in DFIR / incident response
- Strong forensics: Volatility / MemProcFS, FTK / Autopsy, KAPE, plaso/log2timeline, Velociraptor
- Hands-on cloud IR (AWS / Azure / GCP)
- Excellent written communication (you will write client-facing reports under pressure)
- Strong client presence
- Willingness to travel

**Preferred**

- GIAC GCFA + GNFA + GREM
- Public speaking, blog posts, conference talks
- Experience with ransomware negotiation contexts

---

## 6. SOC Manager / Director of Security Operations \u2014 Large enterprise

**Description**

The SOC Manager leads a 15\u201340 person 24x7 SOC + IR + threat hunting + detection engineering team protecting a global enterprise.

**Responsibilities**

- Own the SOC operating model, shifts, escalation paths, SLA / SLO
- Lead vendor strategy for SIEM / SOAR / EDR / MDR / NDR
- Report SOC effectiveness metrics (MTTD, MTTR, dwell time, coverage) to the CISO and Audit Committee
- Drive incident command for major incidents; coordinate with PR, Legal, HR, regulators
- Hire, mentor, develop the team and succession bench
- Budget ownership ($5M\u2013$50M+ depending on enterprise scale)

**Required**

- 10+ years in security operations, with 4+ years managing teams
- Strong technical credibility (former L2/L3 or detection engineer preferred)
- Experience reporting to senior executives and the Board
- Track record building or scaling SOC programs

---

## What recruiters search for (keyword cheatsheet)

- **SIEM**: Splunk (SPL), Microsoft Sentinel (KQL), Google Chronicle (YARA-L), Elastic Stack (KQL/ESQL), IBM QRadar (AQL), Sumo Logic, Exabeam, LogRhythm
- **EDR / XDR**: CrowdStrike Falcon, SentinelOne, Microsoft Defender XDR, Palo Alto Cortex XDR, Carbon Black, Trend Vision One
- **SOAR**: Splunk SOAR (Phantom), Cortex XSOAR, Tines, Torq, Shuffle
- **NDR / Network**: Zeek, Suricata, Snort, Vectra, Darktrace, ExtraHop, Arista Awake
- **Forensics**: Volatility 3, MemProcFS, KAPE, Velociraptor, GRR, Autopsy, FTK, X-Ways, plaso, EZ Tools (Eric Zimmerman)
- **TI / Frameworks**: MITRE ATT&CK, D3FEND, ATLAS (for AI), Diamond Model, Kill Chain, STIX/TAXII, MISP, OpenCTI
- **Detection-as-code**: Sigma, YARA, OSQuery, Splunk ESCU, Elastic Detection Rules, Sentinel Analytics Rules, CrowdStrike CQL
- **Cloud IR**: AWS CloudTrail, GuardDuty, Detective; Azure Sentinel, Defender XDR; GCP SCC, Chronicle
- **Certifications**: Security+, CySA+, BTL1, BTL2, CCD, SC-200, GCIH, GCIA, GCFA, GCFE, GNFA, GCTI, GREM, GCDA, GIAC GMON, SANS FOR508 / FOR578 / FOR500
- **Concepts**: dwell time, MTTD, MTTR, threat hunting, purple teaming, detection engineering, lateral movement, privilege escalation, persistence, exfiltration

---

> Have a SOC / Blue Team JD to add? PR welcome \u2014 see [Contribute.md](../Contribute.md).
