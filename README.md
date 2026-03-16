# Hack The Box - Explosion Machine Pen Test

The Explosion machine on Hack The Box is a beginner-to-intermediate level Linux box designed to introduce users to common exploitation techniques, including service misconfigurations, file inclusion vulnerabilities, and privilege escalation.

## Table of Contents

- [Machine Overview](#machine-overview)
- [Enumeration](#enumeration)
- [Exploitation](#exploitation)
- [Privilege Escalation](#privilege-escalation)
- [Root Flag](#root-flag)
- [Lessons Learned](#lessons-learned)

## Machine Overview

The **Explosion** machine is designed to simulate a real-world penetration test scenario. The goal is to:

- Enumerate open ports and services.
- Identify vulnerabilities to exploit.
- Gain user-level access.
- Escalate privileges to root.
- Capture both user and root flags.

## Enumeration

Start by scanning the machine with tools like `nmap` or `masscan` to identify open ports:

sudo nmap -sV [remote host ip]

https://github.com/TPrzybycien/Hack-the-Box-Explosion-Pen-Test/blob/68fa63930e29185a0d1986041dad28900fa96546/Screenshot%202026-03-15%20222429.png

Paying close attention to the open port 3389 ms-wbt-server 

https://github.com/TPrzybycien/Hack-the-Box-Explosion-Pen-Test/blob/0794a47982b56f66a11d0896715d8fd0ce32a0c6/Screenshot%202026-03-15%20220758.png

## Exploitation 

While looking through the Man pages for xfreerdp, we find a /v option that allows us to specify a hostname 

https://github.com/TPrzybycien/Hack-the-Box-Explosion-Pen-Test/blob/8bd5c0aadcd4d7da8aafd396a062fa493b603ef0/Screenshot%202026-03-15%20230633.png

While testing very common usernames I discovered that "Administrator" may allow us to circumvent the need for a password 

https://github.com/TPrzybycien/Hack-the-Box-Explosion-Pen-Test/blob/0fdd796f5bea69365e490ece1401a1843d10e9e8/Screenshot%202026-03-15%20220951.png

I have successfuly logged in as Administrator 

https://github.com/TPrzybycien/Hack-the-Box-Explosion-Pen-Test/blob/70abba6053408e017efdb0065231cf9c2737c153/Screenshot%202026-03-15%20221012.png

## Root Flag 

The root flag for this machine is located right on the dashboard 

https://github.com/TPrzybycien/Hack-the-Box-Explosion-Pen-Test/blob/f06eb183f13fc343dd866b7ab28b2a13d1163d6d/Screenshot%202026-03-15%20221109.png

## Lession Learned 

The Explosion machine serves as a powerful reminder of the importance of system hardening, proper account security, and rigorous configuration management. By addressing common vulnerabilities and misconfigured services, organizations can significantly improve their overall security posture and reduce the likelihood of exploitation by attackers. This machine reinforced the need to implement security best practices, from restricting access to critical system functions to continuously auditing system configurations.
