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
1. ping:
2. host:
3. dig:
4. nslookup:
5. traceroute:
6. nmap:
7. tcpdump:
8. whois:
9. wget:
10. curl:
11. ifconfig: 

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
Data primitives
Function
Control and loop statements
Understand list and dictionary very well

## Computer Networks Basics

What is this OSI model
Understand TCP/IP model
IPv4 concept and various address formats, CIDR being one example. Understand CIDR range very well. cidr.xyz
If a website or IP address is given, you should be able to gather minimal information using various linux commands or through online resource.
How HTTPs works howhttps.works
How DNS works howdns.works
For other useful networking commands, check Internet and Networking Commands section above.

Think on any of such scenario or concept by keeping security in mind.

## Git Basics

git clone
git add
git commit
git pull
git push
git config
.gitignore

## Cloud Computing Fundamentals
How Cloud Computing is different from Traditional Computing.
What are the various service models and deployment models.
Learn any famous Cloud service provider fundamentals like AWS, Azure, GCP
How you store data in Cloud
How Data security is covered in Cloud
What is Cloud Native solutions
How Logging and Monitoring works here
How you would analyse what's going in Cloud at a central place
How Cloud Security works and what problem it solves
How to secure your Cloud environment better