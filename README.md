CyberSecurity WAF Homelab
1. Detailed Description of DVWA

Damn Vulnerable Web Application (DVWA) is a deliberately insecure PHP/MySQL web application designed for cybersecurity learning and testing.

Purpose:

Learn: Understand the mechanics of common web application vulnerabilities.

Practice: Hone ethical hacking skills in a safe environment.

Test: Evaluate security tools such as Web Application Firewalls (WAFs).

Key Features:

Multiple Vulnerability Types: SQL Injection, Cross-Site Scripting (XSS), Cross-Site Request Forgery (CSRF), Command Injection, and more.

Adjustable Security Levels: Four modes—Low, Medium, High, Impossible—simulate varying levels of defenses.

Educational Focus: Not designed for production but an essential tool for hands-on cybersecurity training.

In this project, DVWA was deployed on the Ubuntu target server, serving as the main vulnerable application to attack and defend.

2. Project Overview

Title: From Attack to Defense: Building a Cybersecurity Home Lab

Objective:
To bridge the gap between theory and practice by:

Attacking a vulnerable application (offensive/red team).

Implementing and validating defensive measures (blue team).

Simulating a real-world cybersecurity scenario in an isolated environment.

3. Lab Architecture & Methodology

The lab followed a two-machine model to mimic a real-world network:

Attacker Machine – Kali Linux

Role: Offensive Security (Red Team).

Tools Used: Built-in Kali tools (browsers, CLI utilities).

Activities: Performed reconnaissance and launched SQL injection attacks on DVWA.

Target Machine – Ubuntu Server

Role: Vulnerable Host (Blue Team target).

Services Configured:

LAMP Stack: Apache, MySQL, PHP.

DVWA: Deployed as the vulnerable app.

SafeLine WAF: Installed as the primary defensive control.

4. Key Activities & Workflow

Setup:

Configured virtual machines with bridged networking.

Installed all required software and services.

Attack Phase (Red Team):

From Kali, launched SQL injection attacks on DVWA’s login page.

Exploited weaknesses to demonstrate real vulnerabilities.

Defense Phase (Blue Team):

Deployed SafeLine WAF on the Ubuntu server.

Configured key security policies:

SQL Injection Detection: Enabled rules to block malicious SQL payloads.

HTTP Flood Protection: Added rules to mitigate DoS attempts by limiting requests per IP.

Authentication Gateway: Placed an additional login layer in front of DVWA.

Validation & Testing:

Repeated attack simulations from Kali.

Verified that the WAF detected, blocked, and logged malicious traffic.

5. Outcome

The project successfully:

Demonstrated the cyber kill chain — from reconnaissance and exploitation to implementing layered defenses.

Showed the effectiveness of WAFs in stopping real-world attack vectors like SQL injection and HTTP floods.

Provided hands-on experience with both offensive and defensive tools in a safe, controlled environment.

Strengthened understanding of practical cybersecurity workflows, bridging the gap between classroom knowledge and real-world application.
