![Common Skills](images/common-skills.png)

It hardly matters whether you are into SoC role or Network Security or AppSec or Cloud Security and so on, there are some common skill sets you should learn and be good at those.
You may skip one or two common skills, if you are aspiring for Risk & Compliance profile (I am not covering anything for them in this repo as of now).

**These skills are:**
1. [Linux Commands](#linux)
2. [Shell Scripting](#shell-scripting)
3. [Python or Go](#python-or-go)
4. [Computer Networks basics](#computer-networks-basics)
5. [Git Bascis](#git-basics)
6. [Cloud Computing Fundamentals](#cloud-computing-fundamentals)

Check my video on Youtube: [Top Tech Skills you should learn](https://www.youtube.com/watch?v=dTZ69l844JM)

## Linux Commands
You don't need to be Linux nerd as a security professional but good hands-on over all linux commands would make you a better security person. 
Below are the three things which I think you should be good at.

_I am not mentioning any Security based Linux OS here, because if you are using those means you already know the important linux commands for your security job.
Also, will not mention anything related to System or OS Security Architecture and it's design_

### 1. Understand Linux structure and its permission
What I understand so far is that in whichever cybersecurity role you are, you would need to work with Linux machine directly or indirectly. So, why not to learn Linux basics as the first skill towards getting closer to cybsersecurity world.
1. Understand how file structure and different permissions work.
2. What are the commands related to permission changes, access controls etc.
3. Where you can upload something malicious, what's this /tmp, /opt, /bin, /etc ...
4. What's the deal with hidden files
5. Understand /etc/shadow, /etc/passwd
6. Where all the logs are stored
7. Not so important, but good to know the difference between debian and rpm based OS

### 2. Common Linux commands
It's not that you should me master at but should be aware all the necessary commands.
Ask yourself for the answers to questions like below:
1. How to list files and folders recursively
2. How to edit a file
3. How to search a file or contents through a file
4. How sudo command works
5. How do I create a subdirectory for which directory doesn't exist yet.
6. How do I combine few linux commands together
7. How do I connect to remote machine
8. How do I see all the running processes
9. How do I compress a file
10. How to check file integrity
11. How to install, uninstall, update and upgrade any application

**Some common commands I can think of are:** 
ls, cd, cp, scp, cat, uname, less, more, sort, ssh, mv, du, df, mount, mkdir, who, locate, chmod, chown, sudo, top, kill, grep, find, sed, awk, ps, zip, tar, service

What else you can think of as common linux commands for everyone? 

### 3. Internet and Networking Commands (May be not so common commands)
These are the commands which are really helpful for security folks. 
I use these commands a lot for my projects and security activities. Think these commands are for basic information gathering phase active or passive

**Some of those Linux Commands are:**
1. ping: Common command that you use when internet is not working ;) Use ping to check if ip or website is reachable. 
2. host: for DNS lookup. mostly we use host domain-name or host ip
3. dig: I consider dig as a big B of host ;)
4. nslookup:
5. traceroute:
6. nmap:
7. tcpdump:
8. whois:
9. wget:
10. curl:
11. ifconfig: 

I will add more details in [Network Security Skills page](network-security.md)

## Shell Scripting
Basic understanding of shell scripting can be common for security engineers. There will be a time where you would need to automate something quickly and if you know linux commands, writing shell script for those tasks would be the quickest part for you.
Many exploits, PoC and useful security scripts are written in shell script as well. 

1. Understand shell prompt in Linux
2. Think in this way, how to write few commands in one place to finish some tasks like installing LAMP, updating some application and restart the server in one go
3. How to execute shell script
4. Understand various shell commands output and how to work with them.
5. Learn if else and loop syntax

You might find something of your interest on [github](https://github.com/search?l=Shell&q=security&type=Repositories)

## Python or Go
1. Data primitives 
2. Function 
3. Control and loop statements 
4. Understand list and dictionary very well
5. List Comprehension
6. zip and map function
7. use of argparse
8. Some useful libraries for security pentest or automation purposes like:
   1. requests
   2. os
   3. regex
   4. python-nmap
   5. scapy
   6. cryptography (hazmat also referred as Hazardous Material)
   7. BeautifulSoup4
   8. faker

## Computer Networks Basics

1. What is this OSI model 
2. Understand TCP/IP model 
3. IPv4 concept and various address formats, CIDR being one example. Understand CIDR range very well. cidr.xyz
If a website or IP address is given, you should be able to gather minimal information using various linux commands or through online resource. 
4. How HTTPs works: [howhttps.works](https://howhttps.works/) 
5. How DNS works: [howdns.works](https://howdns.works/)

For other useful networking commands, check Internet and Networking Commands section above.
Think on any of such scenario or concept by keeping security in mind.

## Git Basics

1. git clone 
2. git add 
3. git commit 
4. git pull 
5. git push 
6. git config 
7. .gitignore

## Cloud Computing Fundamentals
1. How Cloud Computing is different from Traditional Computing. 
2. What are the various service models and deployment models. 
3. Learn any famous Cloud service provider fundamentals like AWS, Azure, GCP 
4. How you store data in Cloud 
5. How Data security is covered in Cloud 
6. What is Cloud Native solutions 
7. How Logging and Monitoring works here 
8. How you would analyse what's going in Cloud at a central place 
9. How Cloud Security works and what problem it solves 
10. How to secure your Cloud environment better
11. How IAM (Identity and Access Management) helps to aid Cloud Security in general