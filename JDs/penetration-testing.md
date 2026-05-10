# Penetration Testing / Red Team Job Descriptions

Representative Pentesting, VAPT, and Red Team JDs from consulting firms, product companies, and internal teams.

> Companion roadmaps: [Web Security](../web-security.md), [API Security](../api-security.md), [Mobile Security](../mobile-security.md), and the central [Security Job Roles hub](../security-job-roles.md)

---

## 1. Junior Penetration Tester / VAPT Analyst (Entry) \u2014 Consulting firm

**Responsibilities**

- Execute web, API, mobile, and network penetration tests under supervision of senior testers
- Use Burp Suite, ffuf, nmap, Nuclei, Metasploit responsibly during engagements
- Document findings with clear reproduction steps, business impact, and remediation
- Defend findings on client closeout calls
- Contribute to internal tooling and methodology updates

**Required**

- 0\u20132 years experience (or proven hands-on track record on HTB / THM / bug bounty)
- Strong OWASP Top 10 knowledge
- Comfort with at least one scripting language (Python)
- Strong written English
- Willingness to learn fast across web, API, mobile, network, cloud

**Nice to have**

- eJPT, OSCP (in progress), PortSwigger BSCP
- 1+ public bug bounty disclosure
- HTB / THM / PortSwigger Academy progression

---

## 2. Penetration Tester (Mid) \u2014 Product company internal team

**Responsibilities**

- Run web, API, mobile, infrastructure, and cloud penetration tests against our own products
- Lead engagements end-to-end \u2014 scoping, testing, reporting, retests
- Build custom Burp extensions, Nuclei templates, and Semgrep rules for org-specific patterns
- Partner with AppSec engineers and engineering teams on remediation guidance
- Conduct internal red-team-lite exercises (e.g., phishing + initial foothold + lateral movement scenarios)
- Mentor junior testers

**Required**

- 3\u20135 years in offensive security
- OSCP (or equivalent demonstrable skill)
- Strong web + API testing background
- Working knowledge of at least one cloud (AWS / Azure / GCP) and Kubernetes
- Strong written communication

**Bonus**

- OSWE, OSEP, OSCE3, GIAC GPEN / GWAPT / GMOB
- Public talks, bug bounty leaderboards, OSS tooling contributions

---

## 3. Senior Red Team Operator \u2014 Mature product / BFSI

**Role**

You will plan and execute multi-month adversary emulation engagements against our own enterprise \u2014 from initial access through lateral movement to objective.

**Responsibilities**

- Plan campaigns using MITRE ATT&CK and threat intelligence on actors targeting our sector
- Execute end-to-end engagements: OSINT, social engineering, initial access, C2, lateral movement, exfiltration simulation
- Build and maintain a private C2 + tooling infrastructure (Cobalt Strike, Sliver, Mythic, custom)
- Run purple-team feedback loops with detection engineering
- Author detailed engagement reports and exec briefings
- Stay within strict legal / ethical scope \u2014 every action authorized in writing

**Required**

- 6\u201310+ years in offensive security with at least 3+ in red team operations
- OSEP, OSCE3, CRTO / CRTO II, or equivalent demonstrated skill
- Deep Windows + Active Directory + Entra ID attack chain knowledge
- Strong C2 operational security (OPSEC) practices
- Comfortable defending decisions in regulator-style review boards

**Preferred**

- Public conference talks (Black Hat, DEF CON, X33fcon)
- OSS red team tooling contributions
- Cloud red team specialization

---

## 4. Pentest / Red Team Manager \u2014 Large enterprise

**Responsibilities**

- Lead a team of 6\u201315 pentesters / red teamers
- Own engagement pipeline, utilization, and quality
- Hire, mentor, and develop testers; participate in advanced interviews
- Be the technical escalation point for difficult engagements
- Report findings and trends to the CISO and leadership

**Required**

- 10+ years in offensive security with 3+ in management
- Strong technical credibility (you've owned high-impact engagements)
- Track record building or scaling pentest teams
- Excellent stakeholder management

---

## What recruiters search for

- **Web / API**: Burp Suite (Pro + extensions), Caido, OWASP ZAP, ffuf, dirsearch, nuclei, sqlmap, mitmproxy
- **Network / infra**: nmap, masscan, Metasploit, CrackMapExec / NetExec, Impacket, BloodHound, Responder, Mimikatz, Rubeus
- **Cloud**: Pacu, Stratus Red Team, ScoutSuite, Prowler, MicroBurst, ROADtools, AzureHound, PurplePanda
- **C2 / Red team**: Cobalt Strike, Sliver, Mythic, Havoc, Brute Ratel, Empire
- **Wireless / physical**: aircrack-ng, Wifite, Bettercap, Proxmark, Flipper Zero
- **Standards**: OWASP Top 10 + API Top 10 + ASVS, PTES, OSSTMM, MITRE ATT&CK
- **Certs**: OSCP, OSWE, OSEP, OSED, OSCE3, eJPT, eCPPT, eWPT / eWPTX, CRTO, CRTO II, CRTE, GPEN, GWAPT, GMOB, BSCP

---

> Have a Pentest / Red Team JD to add? PR welcome \u2014 see [Contribute.md](../Contribute.md).
