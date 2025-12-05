# Cloud Security Detection Engineering: Log4j Exploit Detection & Azure VM Availability Monitoring

This repository contains a hands-on cloud security project focused on
threat detection engineering and operational monitoring using Microsoft
Sentinel and Azure Monitor.\
It demonstrates real-world capabilities in SIEM analytics, alerting,
cloud reliability, and automation, completed as part of the **Manage
Security Operations** specialization.

------------------------------------------------------------------------

## 📌 Project Overview

This project consists of two major SOC activities:

------------------------------------------------------------------------

### 1️⃣ Log4j (Log4Shell) Exploit Detection -- Microsoft Sentinel

Implemented detection capabilities for Log4j exploitation attempts by:

-   Deploying the **Log4j Vulnerability Detection** solution\
-   Configuring the **Log4Shell IP IOC scheduled analytics rule**\
-   Reviewing and enhancing **KQL detection logic**\
-   Adding custom alert details to enrich incident context\
-   Creating automation rules to tag and streamline incident triage

**Result:**\
A functional cloud-based detection mechanism capable of identifying
Log4j exploitation attempts across monitored Azure resources.

------------------------------------------------------------------------

### 2️⃣ Azure VM Availability Monitoring -- Azure Monitor

Configured monitoring and alerting for Azure Virtual Machine (VM) health
using the **VM Availability Metric**.

Key tasks included:

-   Setting monitoring scope for proper resource grouping\
-   Configuring VM availability metrics to monitor uptime\
-   Creating alert rules with relevant thresholds\
-   Building an Action Group to deliver SMS/email notifications\
-   Validating real-time operational alerts in Monitor

**Result:**\
An automated reliability monitoring pipeline ensuring prompt
notifications when VM availability drops.

------------------------------------------------------------------------

## 📂 Repository Structure

    Sentinel-Log4j-Detection/
    │   ├── Log4j-Detection-Overview.md
    │   ├── Analytics-Rule-KQL.txt
    │   ├── Automation-Rule-Config.md
    │   └── Notes.md
    │
    Azure-VM-Availability-Monitoring/
    │   ├── VM-Monitoring-Overview.md
    │   ├── Alert-Rule-Config.md
    │   ├── Action-Group-Setup.md
    │   └── Notes.md
    │
    Assets/
    │   ├── Certificate.png
    │   └── Full-Project-Report.pdf
    │
    README.md

This structure keeps the project clean, technical, and easy to navigate.

------------------------------------------------------------------------

## 🛠 Tools & Technologies Used

-   Microsoft Sentinel\
-   Azure Monitor\
-   Kusto Query Language (KQL)\
-   Analytics Rules (Scheduled)\
-   Azure Action Groups\
-   Automation Rules\
-   Threat Detection Engineering\
-   Cloud Reliability Monitoring

------------------------------------------------------------------------

## 🎯 Skills Demonstrated

✔ Building SIEM detection rules\
✔ Threat detection engineering for real-world vulnerabilities\
✔ KQL log query analysis\
✔ Incident automation (tags, workflows)\
✔ Cloud monitoring via Azure Monitor\
✔ VM availability alerting\
✔ Operational incident response readiness\
✔ Documentation best practices

------------------------------------------------------------------------

## 📄 Full Project Documentation

The full step-by-step project (with explanations) is included in:

**/Assets/Full-Project-Report.pdf**

This includes all tasks, logic, and configurations followed during the
hands-on lab.

------------------------------------------------------------------------

## 🌍 Explore My Learning & Project Ecosystem

### 🔗 LinkedIn -- Professional Insights & Project Highlights

 https://www.linkedin.com/in/prince-richard-o/

### 🎥 YouTube -- Tutorials & Labs

https://www.youtube.com/@SecuredByPrince

### 💻 GitHub -- Security Projects & Automation

https://github.com/SecuredByPrince

### 🧠 X / Medium -- Insights, Learning Updates & Research

https://x.com/SecuredByPrince\
https://medium.com/@SecuredByPrince
