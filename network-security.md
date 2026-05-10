# Network Security Skills and Career Roadmap

> 📘 Recommended study plans: [Common Skills](https://github.com/jassics/security-study-plan/blob/main/common-skills-study-plan.md) · [Product Security](https://github.com/jassics/security-study-plan/blob/main/product-security-study-plan.md).

Network Security is one of the **oldest and most stable** branches of cybersecurity. Every cloud, datacenter, office, and home depends on networking — so skilled network security engineers are always in demand.

## Who is this for?
- Network admins / NOC engineers who want to move into security
- CCNA / Junos / Linux+ certified folks
- Anyone fascinated by packets, firewalls, and how the internet *actually* works

## Pre-requisites (foundation)
1. OSI model, TCP/IP model (know each layer by heart)
2. IPv4, IPv6, CIDR, subnetting (try [cidr.xyz](https://cidr.xyz))
3. Common protocols — DNS, DHCP, ARP, ICMP, HTTP(S), FTP, SSH, SMTP, SMB, NTP, SNMP
4. Routing & switching basics (VLANs, STP, OSPF/BGP at a high level)
5. Linux + Windows networking commands
6. How TLS/SSL handshake works (see [howhttps.works](https://howhttps.works))
7. How DNS works (see [howdns.works](https://howdns.works))

## Career ladder

### Entry level (0–2 years)
**Possible job titles:**

- Network Operations Center (NOC) Analyst
- Network Security Analyst
- Junior Firewall Engineer
- L1 SOC Analyst (network-focused)

**Skills to focus on:**

1. **Packet analysis** — Wireshark, tcpdump basics; read a 3-way handshake on the wire
2. **Firewalls** — start with one vendor (Palo Alto, Fortinet, Check Point, Cisco ASA/FTD); learn rules, NAT, zones
3. **VPN** — IPsec site-to-site, SSL VPN, remote access
4. **IDS/IPS** — Snort, Suricata rules basics
5. **Network scanning** — nmap (host discovery, port scan, NSE scripts)
6. **Common attacks** — ARP spoofing, MITM, DNS poisoning, DDoS basics
7. Logs and SIEM basics — syslog forwarding, log parsing

### Mid level (2–5 years)
**Possible job titles:**

- Network Security Engineer
- Firewall / VPN Engineer
- Cloud Network Security Engineer
- SOC L2 (Network)

**New skills to add:**

1. **Advanced firewall policy design** — segmentation, micro-segmentation
2. **Zero Trust Network Architecture (ZTNA)** — BeyondCorp, ZTNA vendors (Zscaler, Cloudflare, Twingate)
3. **SASE / SD-WAN** — Cato, Palo Alto Prisma, Fortinet, Netskope
4. **Cloud network security** — AWS VPC, Security Groups, NACL, Transit Gateway; Azure NSG, vWAN; GCP VPC
5. **TLS deep dive** — pinning, mTLS, cert lifecycle, ACME, internal PKI
6. **DDoS protection** — Cloudflare, Akamai, AWS Shield
7. **Network forensics** — Zeek, NetFlow / IPFIX, NDR tools (Vectra, Darktrace, ExtraHop)
8. **Wireless security** — WPA2/3, 802.1X, EAP, rogue AP detection
9. **Automation** — Ansible, Terraform for network devices; Python with netmiko / nornir

**Certs to consider:**

- Cisco CCNP Security
- Palo Alto PCNSE
- Fortinet NSE 4–7
- AWS Security Specialty (network-heavy parts)
- (ISC)² CISSP (broader, helpful for promotion)

### Senior level (5–8 years)
**Possible job titles:**

- Senior Network Security Engineer
- Lead Firewall Engineer
- Cloud Network Security Lead
- Zero Trust Engineer

**New focus areas:**

1. **Network architecture design** — HA, multi-region, multi-cloud
2. **Threat modeling** for network designs
3. **Incident response leadership** for network-borne attacks
4. **PCI-DSS / HIPAA segmentation** designs
5. **Vendor evaluation and POCs**
6. **Mentor L1/L2** and review change requests

### Staff / Architect (8+ years)
**Possible job titles:**

- Network Security Architect
- Zero Trust Architect
- Principal Network Security Engineer
- Head of Network Security

**Focus areas:**

- Enterprise-wide network security strategy
- Convergence of network + cloud + identity (SASE, ZTNA)
- Budget ownership, vendor consolidation
- Regulatory alignment (PCI, HIPAA, ISO 27001 network controls)

## Career paths from Network Security

```text
                    Network Security (entry)
                              │
       ┌──────────────┬───────┴───────┬──────────────┐
       ▼              ▼               ▼              ▼
   Firewall /      Cloud Network   SOC / NDR      Network
   VPN Engineer    Security        Detection       Pentester
       │              │               │              │
       ▼              ▼               ▼              ▼
   Zero Trust    Cloud Security   Threat Hunter   Red Team
   Engineer      Architect                         (infra)
       │
       ▼
  Network Security Architect ──► Enterprise Security Architect
```

## Lateral pivots from Network Security
- **→ Cloud Security** — cloud is just networks + IAM + APIs; you already know layer 1
- **→ SOC / DFIR** — network telemetry is the backbone of detection
- **→ Penetration Testing** — internal network pentest, AD attacks
- **→ DevSecOps** — automate network policy as code (Terraform, OPA)
- **→ SRE / Platform Engineering** — reliability-focused track

## Recommended tools to master
- **CLI**: nmap, tcpdump, Wireshark/tshark, dig, nslookup, traceroute, whois, curl, openssl, hping3
- **Firewalls**: iptables/nftables, pf, Palo Alto, Fortinet, Check Point
- **Detection**: Suricata, Zeek, Snort
- **NDR/SIEM**: Splunk, Elastic, Vectra, Darktrace

## AI-augmented Network Security (you need this in 2025+)
AI is rapidly entering network operations — both for defense and inside the network itself.

### Using AI to do network security better
1. **AI-assisted log + pcap analysis** — paste a Wireshark export or zeek log and ask for anomalies
2. **Firewall rule review** — LLMs are surprisingly good at spotting shadowed / redundant / overly permissive rules
3. **Policy translation** — turn business intent ("finance team can reach payroll DB only during business hours") into firewall / NSG / Cloud Armor rules
4. **Suricata / Snort / Zeek rule drafting** from CVE descriptions; you validate against PCAPs
5. **Diagram-to-policy** — AI can read a network diagram and suggest segmentation policy

### Defending against AI-augmented network threats
1. **AI-generated phishing payloads delivered via web / DNS** — detection has to shift behavioral
2. **LLM-driven recon and exploitation** — attacker agents scanning at unusual speeds / patterns
3. **Deepfake voice / video** entering via Teams / Zoom / WebRTC — new detection problem for SOC + network
4. **Egress controls for internal AI agents** — your devs' Copilot / Cursor / ChatGPT traffic is exfiltration risk; categorize and inspect at the egress proxy

### Securing AI traffic flows
1. **AI gateway placement** — inline LLM gateway between users / apps and SaaS AI providers
2. **TLS inspection considerations** for LLM API traffic (privacy + compliance balance)
3. **DLP for AI** — keyword + ML-based detection of sensitive data in outbound AI requests
4. **DNS controls** for AI endpoints — allow-list approved providers, block shadow AI SaaS
5. **Zero Trust for AI workloads** — SPIFFE / SPIRE workload identity, mTLS between AI services

See: [AI Security Career Roadmap](ai-security-career-roadmap.md) · [GenAI Security Study Plan](https://github.com/jassics/security-study-plan/blob/main/genai-security-study-plan.md)

## Recommended books
- *TCP/IP Illustrated, Vol 1* — W. Richard Stevens
- *Network Security Assessment* — Chris McNab
- *Practical Packet Analysis* — Chris Sanders
- *Zero Trust Networks* — Evan Gilman & Doug Barth

---

## Useful Linux Commands / CLI tools for Network Security
1. ping: Common command that you use when internet is not working ;) 
   1. Use ping to check if ip or website is reachable.
   2. Understand the use of ping for ping flood or ICMP flood
   3. try ping with other options i.e. ping -n, ping -c, ping -l, ping -t
   4. Check what is the meaning of ping sweep (Thinking of nmap? try arp -a as well)
2. host: for DNS lookup. 
   1. I mainly use it with -t option to check NS, MX, TXT, CNAME etc. i.e. host -t MX domain-name
   2. host domain-name for IP address
   3. host IP-address for any CNAME
3. dig: I consider dig as a big B of host ;)
   1. `dig domain-name +dnssec +short` to check/verify DNS record. There are many other dig commands for DNS Signature, Verification etc.
   2. `dig domain-name`
   3. `dig domain-name ns` for Nameserver(s)
   4. `dig domain-name mx` for mail server(s)
   5. Server Response as NXDOMAIN might result to domain takeover. Check who is the service provider by running `whois IP | grep "OrgName"`
   6. The following DNS responses warrant further investigation: SERVFAIL or REFUSED.
4. nslookup:
5. traceroute:
6. whois:
7. wget:
8. curl:
9. ifconfig: 


Network Security Tools
1. nmap
2. wireshark
3. tcpdump