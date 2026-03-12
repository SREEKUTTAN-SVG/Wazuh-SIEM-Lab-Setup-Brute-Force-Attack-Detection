# Wazuh SIEM Implementation for Security Monitoring

## Overview

This project demonstrates the implementation of a **Wazuh SIEM (Security Information and Event Management)** lab environment for centralized log monitoring, threat detection, and security analysis.

The lab environment was built using **Ubuntu Server as the Wazuh Manager**, while **Linux and Windows systems were configured as Wazuh Agents**. Logs were collected from monitored endpoints and analyzed through the **Wazuh Dashboard** to detect suspicious activities.

A **brute-force attack simulation** was performed using Hydra to generate security events, allowing the system to detect authentication failures and trigger alerts in real time.

---

## Objectives

* Install and configure **Wazuh SIEM** in a lab environment
* Configure **Linux and Windows endpoints as Wazuh agents**
* Collect and analyze system and authentication logs
* Simulate a **brute-force attack** to test detection capabilities
* Monitor and analyze security alerts using the **Wazuh Dashboard**

---

## Tools and Technologies

* **Wazuh SIEM** – Centralized log monitoring and threat detection
* **Ubuntu Server** – Used for installing and running the Wazuh Manager
* **Kali Linux** – Used as the attacker machine for attack simulation
* **Hydra** – Used to perform brute-force attack testing
* **VirtualBox** – Virtual machine environment used for the lab setup
* **Windows OS** – Endpoint system monitored by the Wazuh agent

---

## Lab Architecture

The lab environment consists of multiple systems connected within a virtual network.

* **Wazuh Manager** – Ubuntu Server
* **Attacker Machine** – Kali Linux
* **Endpoint Systems** – Windows and Linux agents

Logs generated on endpoint machines are forwarded to the **Wazuh Manager**, where they are analyzed using security rules. Alerts are then displayed through the **Wazuh Dashboard** for monitoring and analysis.

---

## Log Collection

The Wazuh agents were configured to monitor important system and authentication logs and forward them securely to the Wazuh Manager.

### Linux Logs

* `/var/log/auth.log`
* `/var/log/syslog`

### Windows Logs

* Security Event Logs
* Login Events

These logs allow the system to detect suspicious activities such as unauthorized login attempts.

---

## Attack Simulation

A **brute-force attack** was simulated using the Hydra tool to test the detection capabilities of the Wazuh SIEM platform.

Example command:

```
hydra -l username -P /usr/share/wordlists/rockyou.txt ssh://TARGET_IP -V
```

The attack generated multiple failed authentication attempts which were captured by Wazuh.

---

## Monitoring and Detection

The Wazuh Manager successfully detected suspicious login attempts and generated alerts in real time.

Detected events included:

* Multiple failed SSH login attempts
* Authentication failures
* Suspicious login patterns

Alerts were visualized through the **Wazuh Dashboard Security Events panel**.

---

## MITRE ATT&CK Mapping

The detected brute-force activity was mapped to the **MITRE ATT&CK Framework**.

* **Technique:** T1110 – Brute Force
* **Tactic:** Credential Access

This mapping helps security analysts understand the attack behavior and classification.

---

## Results

The monitoring system generated a large number of alerts during the attack simulation.

Key observations:

* High number of authentication failures
* Alert spike during attack time
* Successful detection of brute-force behavior

The dashboard provided visual graphs and event data to analyze the attack activity.

---

## Remediation

To mitigate brute-force attacks, the following security measures are recommended:

* Implement account lockout policies
* Enable multi-factor authentication (MFA)
* Restrict SSH access using firewall rules
* Use strong password policies
* Regularly update systems and security patches

---

## Challenges Faced

During the lab setup, several challenges were encountered:

* Network configuration issues between virtual machines
* Firewall blocking required ports
* Resource limitations when running multiple virtual machines
* Retrieving the auto-generated Wazuh dashboard password

These challenges were resolved through troubleshooting and configuration adjustments.

---

## Conclusion

This project successfully demonstrates the implementation of **Wazuh SIEM for centralized log monitoring and threat detection**.

The system effectively detected brute-force attack attempts by analyzing authentication logs and generating alerts through the Wazuh Dashboard. This experiment highlights the importance of SIEM solutions in identifying and responding to cyber threats in real time.

---

## Repository Contents

```
/screenshots
/report
README.md
```

* **screenshots/** – Dashboard and attack simulation images
* **report/** – Full project report (PDF)
* **README.md** – Project overview and documentation

---

## Author

Cybersecurity Student
Project: Wazuh SIEM Implementation
