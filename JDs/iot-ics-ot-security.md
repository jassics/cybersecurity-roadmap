# IoT / ICS-OT Security Job Descriptions

Representative job descriptions for IoT, embedded device, and Industrial Control Systems / Operational Technology (ICS-OT) security roles. These are paraphrased composites; numbers and tools mirror real postings in 2024–2025.

> Companion roadmap: [IoT / ICS-OT Security Career Roadmap](../iot-ics-ot-security.md)

---

## 1. Junior IoT Security Engineer (Entry) — Consumer electronics OEM

**Responsibilities**

- Perform security assessments of connected devices (Wi-Fi, BLE, Zigbee, Thread, Matter)
- Conduct firmware extraction (UART, SPI flash dumps, JTAG) under guidance
- Run static analysis on binaries and Linux-based firmware images
- Test mobile companion apps and cloud APIs as part of the device ecosystem
- Document findings against OWASP IoT Top 10 / IoT Security Verification Standard (ISVS)
- Help triage external vulnerability reports (PSIRT support)

**Required**

- 1–2 years in security, embedded, or QA
- Comfortable with Linux, Python, and basic C
- Familiarity with at least one wireless protocol (Wi-Fi / BLE / Zigbee)
- Experience with Burp Suite or similar for HTTP / API testing
- Bachelor's in CS / EE / ECE or equivalent

**Preferred**

- Hands-on with binwalk, Ghidra, soldering basics, logic analyzers
- TryHackMe / HackTheBox profile, IoTGoat or DVID experience

---

## 2. IoT Security Engineer / Pentester (Mid) — Connected medical device company

**Responsibilities**

- Lead end-to-end security assessments of new device models pre-launch
- Perform hardware analysis: chip identification, glitching, side-channel review
- Reverse-engineer firmware and protocol stacks
- Threat-model devices following STRIDE / IEC 62443-4-1
- Drive secure boot, secure update, and key-provisioning reviews with engineering
- Coordinate with regulatory team on FDA premarket cybersecurity submissions

**Required**

- 4–6 years in IoT / embedded / firmware security
- Strong skills with Ghidra / IDA, Frida, OpenOCD, Saleae logic
- Deep understanding of cryptography integration (TLS, secure boot, X.509, signing)
- Familiarity with FDA premarket cyber guidance, IEC 62304, MDCG 2019-16
- BLE / LoRa / cellular IoT protocol experience a plus

**Preferred**

- OSCP, Offensive Security Exploit Developer, or Practical Hardware Hacker
- Public CVEs / conference talks (DEF CON IoT Village, hardwear.io)

---

## 3. Senior Embedded / Hardware Security Researcher — Semiconductor / SoC vendor

**Responsibilities**

- Perform deep vulnerability research on SoCs, secure elements, TPMs, TEEs
- Build custom rigs for fault injection (voltage / clock / EM glitching) and side-channel (DPA, EM)
- Reverse-engineer ROM, bootloaders, TrustZone / SGX-equivalent firmware
- Coordinate disclosure with downstream customers (OEMs, cloud providers, OS vendors)
- Author internal threat models for new silicon revisions
- Mentor junior researchers; represent the team at top-tier conferences

**Required**

- 7+ years in hardware / embedded / low-level security
- Strong skills with ChipWhisperer, JTAGulator, Saleae, oscilloscopes
- Deep ARM (Cortex-M / Cortex-A) and/or RISC-V internals
- Cryptographic implementation review — constant-time analysis, side-channel reasoning
- Track record of CVEs / publications in the space

**Preferred**

- PhD or equivalent practical record (DEF CON / Black Hat / USENIX talks)
- Familiarity with FIPS 140-3 and Common Criteria evaluations

---

## 4. ICS / OT Security Analyst (Entry) — Power utility

**Responsibilities**

- Monitor OT-specific SIEM / NDR (Dragos, Claroty xDome, Nozomi Guardian) for plant networks
- Triage alerts and coordinate with plant control engineers (avoid disrupting operations)
- Maintain asset inventory of PLCs, RTUs, HMIs, historians across multiple sites
- Perform log review for jump servers, OT firewalls, and remote-access gateways
- Support compliance evidence for NERC CIP / IEC 62443

**Required**

- 1–3 years in IT / network security / SOC
- Curiosity for industrial protocols (Modbus, DNP3, IEC 61850, OPC UA)
- Strong networking fundamentals
- Willingness to spend time in plant / substation environments
- Comfort with shift-based work for some roles

**Preferred**

- GICSP (GIAC Industrial Cyber Security Professional)
- ISA/IEC 62443 Cybersecurity Fundamentals Specialist
- Experience with Wireshark dissectors for OT protocols

---

## 5. ICS / OT Security Engineer (Mid) — Oil & gas major

**Responsibilities**

- Lead OT network segmentation projects following Purdue Reference Model
- Deploy and tune OT-specific tools (Dragos, Claroty, Nozomi, Tenable.OT)
- Implement secure remote access for vendors (Cyolo, Xage, Claroty Secure Remote Access)
- Coordinate patching cycles with plant turnarounds (typically 1–2× per year)
- Run tabletop exercises with control-room operators using realistic OT scenarios (TRITON, Industroyer, Stuxnet families)
- Liaise with engineering on safety-instrumented systems (SIS) cybersecurity

**Required**

- 5–8 years across IT and OT security
- Strong knowledge of industrial protocols and vendor stacks (Siemens, Rockwell, Schneider, ABB, Emerson, Yokogawa, Honeywell)
- Solid understanding of Purdue model, IEC 62443 zones & conduits
- Comfort working closely with process / control engineers
- Field readiness — willingness to travel to remote sites

**Preferred**

- GRID (GIAC Response and Industrial Defense)
- GICSP, ISA/IEC 62443 Risk Assessment / Design Specialist
- Background in process / electrical / instrumentation engineering

---

## 6. Senior ICS / OT Threat Hunter — Critical infrastructure (water / power / transport)

**Responsibilities**

- Build OT-specific detection content for ICS protocols and TTPs (Dragos / Sigma / Zeek)
- Hunt for living-off-the-land in OT (engineering workstations, jump hosts, vendor laptops)
- Coordinate with national CSIRT / sector ISAC / CISA for threat intel
- Author OT incident playbooks that prioritize **safety and availability** over confidentiality
- Lead red/purple team exercises against OT lab environments
- Brief executives and regulators on threat landscape (CISA advisories, Volt Typhoon, Sandworm, etc.)

**Required**

- 8+ years in security, including 4+ in OT / ICS
- Deep knowledge of MITRE ATT&CK for ICS
- Strong ability to read network traffic for industrial protocols
- Hands-on experience responding to at least one significant OT incident
- Strong communication — you'll talk to plant managers and CISOs in the same week

**Preferred**

- GRID, GICSP, GREM
- Public speaking at S4, SANS ICS Summit, or Black Hat ICS Village

---

## 7. ICS / OT Security Architect — Manufacturing conglomerate (multi-site)

**Responsibilities**

- Define OT cybersecurity reference architecture across global plants
- Standardize zones, conduits, DMZs, secure remote access, and patch strategy
- Integrate IT / OT SOC with shared SIEM and clear handoff playbooks
- Pick and roll out OT visibility platform across dozens of plants
- Lead M&A integrations on the OT side (often the slowest, riskiest part)
- Influence corporate risk committee and board on OT cyber risk
- Champion compliance with IEC 62443, NIST SP 800-82, NIS2, NERC CIP (where applicable)

**Required**

- 10+ years across IT and OT security with at least 5 in OT
- Strong architecture / threat-modeling chops
- Vendor-agnostic but comfortable with multiple ICS stacks
- Excellent communicator; comfortable in C-suite and shop floor

**Preferred**

- ISA/IEC 62443 Expert, GRID, CISSP-ISSAP
- Prior plant or operations background (huge bonus)
- Experience with insurance / regulator engagements

---

## 8. IoT Product Security PM / Lead — Enterprise IoT platform vendor

**Responsibilities**

- Own IoT product security program across firmware, cloud, and mobile components
- Drive SDLC adoption for embedded teams (threat modeling, secure coding, fuzzing, SBOMs)
- Lead PSIRT process and external coordination (CVE assignment, advisories)
- Partner with regulatory team on EU CRA, FCC, UK PSTI, US Cyber Trust Mark
- Set roadmap for secure boot, signed updates, attestation, and key management
- Speak to enterprise customers about device security

**Required**

- 8+ years across product / IoT / embedded security
- Strong technical depth + program management ability
- Familiarity with EU Cyber Resilience Act, ETSI EN 303 645, NIST IR 8259, ANSSI guidelines
- Proven ability to ship and harden a connected product line

**Preferred**

- Public speaking, prior leadership of PSIRT
- Background in hardware / firmware engineering

---

## Recruiter keyword cheatsheet

When tailoring a resume for IoT / ICS-OT roles, recruiters scan for:

- **Protocols** — Modbus, DNP3, IEC 61850, OPC UA, BACnet, Profinet, HART, S7, EtherNet/IP, BLE, Zigbee, Thread, Matter, LoRaWAN, MQTT, CoAP
- **Vendors / stacks** — Siemens, Rockwell, Schneider, ABB, Emerson, Honeywell, Yokogawa, GE
- **OT security platforms** — Dragos, Claroty (xDome / CTD / SRA), Nozomi (Guardian / Vantage), Tenable.OT, Microsoft Defender for IoT, Forescout SilentDefense, Armis
- **Hardware tools** — Ghidra, IDA, binwalk, OpenOCD, JTAGulator, Saleae, ChipWhisperer, HackRF, Ubertooth, Proxmark, RTL-SDR, Bus Pirate
- **Standards / regs** — IEC 62443, NIST SP 800-82, NIST IR 8259, ETSI EN 303 645, ISA/IEC 62443-2-4, ISA/IEC 62443-4-1/4-2, NERC CIP, NIS2, EU Cyber Resilience Act, UK PSTI, FDA premarket cyber guidance, MDCG 2019-16
- **Frameworks** — MITRE ATT&CK for ICS, Purdue Reference Model, ISA-95
- **Certs** — GICSP, GRID, GREM, ISA/IEC 62443 Cybersecurity Specialist (Fundamentals / Risk Assessment / Design / Maintenance / Expert), CISSP, CEH, OSCP

> **Tip:** Most OT shops still hire IT-style security folks who *want* to learn OT. The fastest entry is to combine an existing security role with an ICS lab (open-source Modbus / DNP3 simulators, second-hand PLCs from eBay) and a GICSP cert.

See also: [SOC / Blue Team JDs](soc-blue-team.md) · [Network Security JDs](network-security.md) · [Security Architect JDs](security-architect.md)
