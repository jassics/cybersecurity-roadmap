# Application Security Interview Questions

I will share interview questions and possibly with some examples, scenarios on AppSec which would be different for [web security](web-security-interview-questions.md) or penetration testing.

**This space will more focus on:**

1. Secure Code Review
2. Threat Modeling
3. Secure Coding
4. Secure Development
5. And anything that is defensive in nature and developer centric. For everything else related to [web security we have another page](web-security-interview-questions.md).

If you are interviewing someone for Application Security Engineer role, could be juinor, senior or architect level.
You can always start questions based on the person's experience in AppSec. However, below questions can be always interesting and will help you to understand the candidate better technically.
Soft skills, team player, presentation skills, communication skills are out of the scope of this space.

## What do you think about the good password?
    
This question looks very similar, but can help the interviewer to understand if the person has experience with password management related skills or not. 
    
This question will help you to drill down to more specific questions to understand the competence of the candidate:
   1. What is complex password
   2. Should the password complexity be same for admin and user
   3. How do you save the password in Database, encrypted or hashed or plain text
   4. Do you use salt? Is it same for all the password? is it random in nature per user?
   5. How do you make your code safe for password attacks?

## How do you stop bruteforce attack on login/signup/forgot password page(s)?
This question helps you to understand if the person is aware of secure code development and secure design for such features and how far he/she can think.
Check if the person talks about:

1. Captcha 
2. CSRF token
3. Rate Limiting
4. MFA
5. Alert and Monitor for such anomalous behavior
6. Account Lockout after n failed attempts

## What happens when you type google.com on browser
This question is just to check if the person understands the behind the curtain scene like url to IP conversion, DNS involvement, server response and so on.
Listen the interviewee and see if he/she mentions below things:
1. How DNS resolves the url 
2. TCP 3 way handshake
3. How HTTPS work and what's its advantages
4. How to prevent the application from MiTM (Man in The Middle Attack)

## How SSL/TLS actually makes my content secured over the internet
This question is the extension of previous question to understand if the person understands:

1. How client server hello established
2. How key exchange happens i.e. public key or certificate
3. Is it symmetric or asymmetric encryption or both and when it is used 
4. Talks about Certificate Signing Request (CSR)
5. What are weak ciphers and what are good SSL Cipher Suites
6. Able to use openssl command to see the details of ssl information
7. Can explain ssl format like this: **TLS_ECDHE_RSA_WITH_AES_128_GCM_SHA256**
8. TLS 1.2 or TLS 1.3 and why? 
9. What is PFS (Perfect Forward Secrecy) and why it is used?
10. Why https enabled website still gets hacked?

## How you would make developers aware and involved for secure code development?
This question would help you to understand if the person has delivered any training, presentaed slides, gave demo, delivered secure coding practices workshops.
See if person talks about:

1. OWASP ASVS (Application Security Verification Standard)
2. OWASP Top 10 2017/2021
3. OWASP Secure Review with some examples
4. Secure Design Principles
5. Then you can go little deeper like what difficulties you faced while giving training to them on secure code design, principles etc.
6. How do you make sure developers follow what you taught or made aware? IDE plugin, git actions, SAST tools etc?

## Which one would you prefer and why? Manual secure code review or automated or both ?
## Which tools have you used for SAST?
## What is the difference between SAST and SCA?
## How well you understand SQLi (SQL Injection)?
## Do you understand the key difference between encryption, hashing, salt, obfuscation and encoding?
## What you should check if the website is damn slow suddenly?
## Explain how do you handle AuthN and AuthZ?
## How you implemented CSP? Do you think it adds extra security for a web application? How?
## How do you handle typical developer and security clash sittation?