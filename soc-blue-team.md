# SOC / Blue Team Career Roadmap

> 📘 Recommended study plans: [Blue Team, Detection & Response](https://github.com/jassics/security-study-plan/blob/main/blue-team-detection-response-study-plan.md) · [Reverse Engineering & Malware Analysis](https://github.com/jassics/security-study-plan/blob/main/reverse-engineering-malware-security-study-plan.md) · [Common Skills](https://github.com/jassics/security-study-plan/blob/main/common-skills-study-plan.md).

SOC (Security Operations Center) and the broader Blue Team are the **defensive backbone** of cybersecurity. If offensive security is about *finding* problems, blue team is about *detecting, responding to, and stopping* them — 24×7. Most large enterprises hire blue teamers in much higher numbers than pentesters, so this is one of the **highest-volume entry points** into the industry.

## Who is this for?
- Freshers / career switchers wanting a fast entry into security (SOC L1 is the most common first job)
- Sysadmins / network admins moving toward security
- Helpdesk / NOC engineers wanting upward mobility
- Pentesters who want to "switch sides" and build defenses

## Pre-requisites (foundation)
1. Networking — TCP/IP, DNS, HTTP, common ports, firewall basics
2. Windows + Linux at user/admin level (Event Viewer, journald, syslog)
3. Active Directory basics — users, groups, GPOs, Kerberos, NTLM
4. Cloud basics (at least one of AWS / Azure / GCP)
5. Scripting — PowerShell + Python (regex is non-negotiable)
6. OWASP Top 10 awareness (so you can recognize web attacks in logs)
7. Familiarity with **MITRE ATT&CK** matrix

## Career ladder

### Entry level (0–2 years) — SOC L1
**Possible job titles:**

- SOC Analyst L1
- Security Operations Analyst (Junior)
- Incident Response Analyst (Junior)
- Threat Detection Analyst

**Day-to-day:**

- Monitor SIEM dashboards / alert queues
- Triage alerts (true positive / false positive / benign true positive)
- Escalate confirmed incidents to L2
- Run basic enrichment (VirusTotal, AbuseIPDB, WHOIS, GreyNoise)
- Document everything in a ticketing system

**Skills to focus on:**

1. **SIEM fluency** — Splunk SPL, Microsoft Sentinel KQL, Elastic KQL, Chronicle YARA-L, IBM QRadar AQL
2. **Log sources** — Windows Event Logs (Security 4624/4625/4688/4697/4720), Sysmon, Linux auth.log, web server logs, EDR telemetry, AWS CloudTrail, O365/Entra ID audit logs
3. **EDR/XDR** — CrowdStrike Falcon, SentinelOne, Microsoft Defender, Carbon Black; how to read alerts, isolate hosts, pull artifacts
4. **MITRE ATT&CK** — map alerts to tactics & techniques
5. **Phishing analysis** — header inspection, URL detonation (URLScan, any.run), attachment sandboxing
6. **Malware analysis 101** — hashes, strings, PE basics, dynamic in a sandbox
7. **Incident ticketing & runbooks** — ServiceNow, TheHive, Jira; following playbooks
8. **Common detections** — failed logins → brute force, beaconing, lateral movement (PSExec, WMI), DNS tunneling

**Entry certs:**

- CompTIA Security+ — almost mandatory in many regions
- CompTIA CySA+ — directly SOC-aligned
- Splunk Core Certified User / Power User
- Microsoft SC-200 (Security Operations Analyst)
- Blue Team Level 1 (BTL1) — well-respected hands-on cert
- CCD (Certified CyberDefender) — affordable, hands-on

### Mid level (2–5 years) — SOC L2 / IR
**Possible job titles:**

- SOC Analyst L2
- Incident Responder
- Threat Hunter (Junior)
- Detection Engineer (Junior)

**Day-to-day:**

- Lead investigations escalated from L1
- Pivot across data sources (network + endpoint + identity + cloud)
- Build/tune detection rules
- Contain & eradicate incidents
- Write incident reports for management

**New skills to add:**

1. **Deep investigation** — timeline reconstruction, root-cause analysis
2. **Digital Forensics basics** — disk imaging (FTK, dd), memory forensics (Volatility, MemProcFS), Windows artifacts (MFT, USN journal, AmCache, Prefetch, ShimCache, RecentDocs)
3. **Network forensics** — full packet capture analysis (Wireshark, Zeek), NetFlow analysis
4. **Detection engineering** — Sigma rules, YARA, custom Splunk/KQL detections, MITRE-driven coverage gap analysis
5. **Threat hunting** — hypothesis-driven hunts (e.g., "find unsigned binaries running from %TEMP%"); use of Jupyter / msticpy
6. **Cloud incident response** — AWS/Azure/GCP IR playbooks, IAM compromise containment, snapshot forensics
7. **Adversary emulation knowledge** — read Atomic Red Team / Caldera tests so you can detect them
8. **Scripting for automation** — Python + APIs (SIEM, EDR, TI feeds)
9. **Threat Intel consumption** — IOCs, TTPs, STIX/TAXII, MISP

**Certs to consider:**

- GIAC GCIH, GCIA, GCFA, GCFE, GNFA, GCTI (one or two of these, not all)
- Blue Team Level 2 (BTL2)
- SANS FOR508 / FOR578 / FOR500 (associated GIAC)
- eCIR / CCFE (eLearnSecurity / Mile2 alternatives)
- AWS Security Specialty (cloud IR side)

### Senior level (5–8 years) — SOC L3 / Senior IR / Detection Engineer
**Possible job titles:**

- SOC Analyst L3
- Senior Incident Responder / Lead IR
- Senior Threat Hunter
- Detection Engineering Lead
- DFIR Consultant

**New focus areas:**

1. **Incident command** — lead breach response from triage to post-mortem
2. **Threat hunting program** design — hypotheses backlog, coverage tracking
3. **Detection-as-code** — git-based rule repos, CI testing of detections, dispatch pipelines
4. **Purple team exercises** — co-design with red team, close gaps
5. **Threat modeling for detection** — what should we be able to detect that we can't?
6. **Tabletop exercises** with execs
7. **Mentor L1/L2**, hire, and train
8. **Vendor evaluation** — SIEM/EDR/SOAR/NDR POCs

### Staff / Principal / Architect (8+ years)
**Possible job titles:**

- SOC Architect
- Principal Detection Engineer
- Principal Incident Responder
- Director of Threat Detection & Response
- Head of SOC / Head of CIRT

**Focus areas:**

- SOC reference architecture (people, process, tech)
- Build vs. buy vs. MDR (Managed Detection & Response) strategy
- Log pipeline & cost engineering (Cribl, Vector, custom)
- Metrics that matter — MTTD, MTTR, dwell time, true-positive rate
- Industry presence — DFIR Summit, BSides, SANS talks

## Specialization branches

### DFIR (Digital Forensics & Incident Response)
- Memory + disk + network forensics; chain of custody; expert witness; ransomware negotiation contexts
- Certs: GCFA, GCFE, GNFA, GREM

### Threat Intelligence (CTI)
- Strategic / operational / tactical TI; attribution; intelligence requirements (PIRs)
- Certs: GCTI, CREST CRTIA

### Detection Engineering
- Sigma, YARA, detection-as-code, ATT&CK coverage maps, telemetry engineering
- Heavy code + data engineering work; closest blue-team role to DevSecOps

### Threat Hunting
- Hypothesis-driven, ML-assisted; closely tied to TI and DE
- Lots of notebook work — Jupyter, msticpy, KQL/SPL pipelines

### Purple Team
- Bridges red + blue; coordinates emulations and detection improvement cycles
- Skills from both sides; great staff-level role

## Career paths from SOC / Blue Team

```text
                       SOC L1 (entry)
                              │
                              ▼
                       SOC L2 / IR
                              │
       ┌──────────────┬───────┴───────┬──────────────┐
       ▼              ▼               ▼              ▼
     DFIR        Detection         Threat          Threat
                 Engineering       Hunting         Intelligence
       │              │               │              │
       ▼              ▼               ▼              ▼
   Senior IR /   Detection Eng.   Senior Threat   CTI Lead
   DFIR Lead     Lead             Hunter
                                                   │
       └──────────────┬────────────────────────────┘
                      ▼
              Purple Team Lead / SOC Architect
                      │
                      ▼
        Head of SOC / Director Threat Detection & Response
```

## Lateral pivots from SOC / Blue Team
- **→ Penetration Testing / Red Team** — most pentesters start as blue teamers; the reverse is also common
- **→ DevSecOps** — detection-as-code skill set translates directly to pipeline automation
- **→ Cloud Security Engineering** — cloud IR opens the door
- **→ GRC** — incident metrics, audit support, policy work
- **→ Security Architecture** — natural senior IC move
- **→ Sales Engineering** — vendors love SOC L3s who can speak customer

## Recommended tools to master
- **SIEM**: Splunk, Microsoft Sentinel, Elastic, Chronicle, IBM QRadar, Sumo Logic
- **EDR / XDR**: CrowdStrike Falcon, SentinelOne, Microsoft Defender XDR, Palo Alto Cortex XDR, Carbon Black
- **SOAR**: Splunk SOAR (Phantom), Palo Alto Cortex XSOAR, Tines, Torq, Shuffle (open source)
- **NDR**: Zeek, Suricata, Vectra, Darktrace, ExtraHop
- **Forensics**: Volatility 3, MemProcFS, Autopsy, FTK, KAPE, Velociraptor, GRR, plaso/log2timeline
- **Threat Intel platforms**: MISP, OpenCTI, ThreatConnect, Anomali, Recorded Future
- **Detection-as-code**: Sigma, YARA, Elastic Detection Rules, Sentinel Analytics Rules, Splunk ESCU

## AI-augmented Blue Team (you need this in 2025+)
AI is one of the biggest leverage points in defensive work.

### Using AI to defend better
1. **Alert triage and summarization** — LLMs summarize event chains, suggest likely TTPs, draft analyst notes
2. **Detection content generation** — first-draft Sigma / KQL / SPL from a CVE writeup or DFIR Report case study
3. **Hunt hypothesis generation** — brainstorm ATT&CK technique coverage gaps with an LLM
4. **Log parsing / regex / KQL help** — huge time saver during investigations
5. **Phishing analysis** — LLMs are surprisingly good at classifying suspicious emails (with caution — attackers use AI too)
6. **Tabletop and post-incident report drafts** — first 80% from AI, last 20% from you

### Defending against AI-powered attacks
1. **AI-generated phishing** — perfect grammar, victim-specific context, multilingual. Detection has to shift from "looks wrong" to behavioral / DMARC / link reputation.
2. **Voice cloning + deepfake vishing** — BEC + CEO fraud now passes a phone call test
3. **AI-assisted malware** — polymorphic strings, custom packers; YARA rules must focus on behavior, not strings
4. **LLM-driven recon at scale** — attackers crawl LinkedIn / GitHub via agents
5. **Detecting AI agent abuse inside your env** — unusual API call patterns from Copilot-like tools, exfil via chat sessions

### Securing the AI tools your org uses (you're often the SOC owner of this)
1. Log ingestion of LLM gateway, Copilot Audit Logs, ChatGPT Enterprise logs into your SIEM
2. Build detections for sensitive data hitting AI endpoints
3. Define IR playbooks for compromised AI agent credentials
4. Coordinate with GRC on AI usage policy + DLP

See: [AI Security Career Roadmap](ai-security-career-roadmap.md) · [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

## Recommended hands-on labs
- **BlueTeamLabs.online** (BTLO) — gold-standard SOC scenarios
- **LetsDefend.io** — realistic SOC simulator
- **CyberDefenders** — DFIR / blue team challenges (free + paid)
- **TryHackMe SOC Level 1 / 2** paths
- **HackTheBox Sherlocks** — DFIR investigations
- **RangeForce**, **Immersive Labs** (often via employer)
- **DFIR.training** — curated content + sample cases

## Recommended books
- *Blue Team Handbook: Incident Response Edition* — Don Murdoch
- *Practical Threat Intelligence and Data-Driven Threat Hunting* — Valentina Costa-Gazcón
- *Applied Incident Response* — Steve Anson
- *The Practice of Network Security Monitoring* — Richard Bejtlich
- *Crafting the InfoSec Playbook* — Jeff Bollinger et al.
- *Intelligence-Driven Incident Response* — Scott Roberts, Rebekah Brown

## Recommended creators / communities
- SANS DFIR blog & DFIR Summit talks (free on YouTube)
- The DFIR Report (incident write-ups, gold mine)
- Florian Roth (Sigma project), Olaf Hartong (Sysmon configs)
- r/blueteamsec subreddit
- BlueTeamCon, FIRST conferences

## Next step
1. Pick **one SIEM** (Splunk or Sentinel) and grind 50+ hours of hands-on labs.
2. Do **at least 20 BTLO / LetsDefend** investigations end-to-end.
3. Read **one DFIR Report** writeup per week and try to write the corresponding detection (Sigma rule).
4. Build a tiny **home lab**: AD domain + 1 Linux server + Sysmon + Wazuh/ELK; attack it with Atomic Red Team; detect yourself.
