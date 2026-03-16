# Hack The Box - Explosion Machine Pen Test

The Explosion machine on Hack The Box is a beginner-to-intermediate level Linux box designed to introduce users to common exploitation techniques, including service misconfigurations, file inclusion vulnerabilities, and privilege escalation.

## Table of Contents

- [Machine Overview](#machine-overview)
- [Enumeration](#enumeration)
- [Exploitation](#exploitation)
- [Privilege Escalation](#privilege-escalation)
- [Root Flag](#root-flag)
- [Lessons Learned](#lessons-learned)
- [References](#references)

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

