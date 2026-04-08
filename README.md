 SIEM Implementation using Wazuh for Threat Detection

 Overview
 ---------

This project demonstrates the implementation of a Security Information and Event Management (SIEM) system using Wazuh. The objective is to monitor system logs, detect security threats, and analyze suspicious activities in a controlled lab environment.


---

 Objectives
------------

Implement a SIEM solution using Wazuh

Collect and monitor logs from multiple systems

Simulate a real-world attack (SSH brute force)

Detect threats using log analysis and rule-based alerts

Perform threat analysis using Wazuh Dashboard



---

 Tools and Technologies
-----------------------

Wazuh SIEM

Ubuntu Server (Wazuh Manager)

Kali Linux (Attacker Machine)

Windows OS (Agent System)

Hydra (Brute Force Tool)

VirtualBox (Virtualization)



---

Lab Architecture
------------------

Kali Linux (Attacker)
        │
        ▼
Wazuh Agent (Windows)
        │
        ▼
Wazuh Manager (Ubuntu Server)
        │
        ▼
Wazuh Dashboard (Monitoring & Analysis)


---

 Implementation Steps
----------------------

1️. Installation & Configuration

Installed Wazuh Manager on Ubuntu Server

Installed Wazuh Agents on Windows and Kali Linux

Configured agents to communicate with the manager


2️. Log Collection

System and authentication logs collected from agents

Logs forwarded to Wazuh Manager for centralized monitoring


3️. Attack Simulation

Performed SSH brute force attack using Hydra

Targeted login authentication on the system


4️. Monitoring & Threat Detection

Wazuh analyzed logs using decoders and rules

Multiple failed login attempts triggered alerts

Alerts monitored through the Wazuh Dashboard



---

 Threat Analysis
-----------------

Detected high number of failed SSH login attempts

Identified brute force attack pattern

Alerts mapped to MITRE ATT&CK Technique: T1110 (Brute Force)



---

 Findings
-----------

Total alerts generated: 2291

Failed SSH login attempts: 1832

Attack type: SSH Brute Force

Detection: Real-time alerting using Wazuh



---

 Remediation Measures
----------------------

Implement account lockout policies

Enable multi-factor authentication (MFA)

Enforce strong password policies

Restrict SSH access to trusted IPs

Keep systems updated with latest security patches



---

 Challenges Faced
------------------

Agent installation and configuration issues

Log collection delays

Dashboard setup complexity

Initial difficulty in understanding SIEM workflow



---

 References
--------------

https://documentation.wazuh.com

https://attack.mitre.org

https://ubuntu.com/server/docs

https://github.com/vanhauser-thc/thc-hydra



---

 Conclusion
------------

This project successfully demonstrates how a SIEM system can be used to detect and analyze security threats in real time. Wazuh proved to be an effective open-source solution for log monitoring, threat detection, and incident analysis.


---

 Author
--------

SREEKUTTAN PS
Cyber Security Enthusiast


---

⭐ If you found this useful

Give this repository a ⭐ and connect with me on Linkedin(https://in.linkedin.com/in/sreekuttan-ps-)
