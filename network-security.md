Some useful Linux Commands or CLI tools for Network Security

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