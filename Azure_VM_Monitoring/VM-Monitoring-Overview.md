# Azure VM Availability Monitoring -- Overview

This document provides a detailed overview of the Virtual Machine (VM)
Availability Monitoring configuration implemented using **Azure
Monitor**.\
The goal of this project was to set up real-time detection and alerting
when an Azure VM becomes unavailable, supporting operational continuity
and rapid response.

------------------------------------------------------------------------

## 📌 Objective

To create a monitoring and alerting pipeline capable of:

-   Tracking VM uptime using Azure's **VM Availability Metric
    (Preview)**
-   Generating alerts when availability drops
-   Notifying stakeholders through **email/SMS**
-   Supporting cloud operations and business continuity

This ensures high reliability and rapid detection of service outages.

------------------------------------------------------------------------

## 🛠 Step-by-Step Implementation

### 1️⃣ Selecting the Monitoring Scope

The first step was to define the resource scope for metric analysis.

**Actions performed:** - Opened **Azure Monitor → Metrics** - Selected
the appropriate **Subscription or Resource Group** - Filtered resource
types to **Virtual Machines** - Selected the VM used in this project:
**IPO-VM**

This ensures the metrics explorer focuses only on the relevant VM.

------------------------------------------------------------------------

### 2️⃣ Selecting the VM Availability Metric

On the Metrics page:

-   From the *Metric* dropdown, selected **VM Availability Metric
    (Preview)**
-   Confirmed that the visualization reflects VM uptime values

The VM availability metric reports whether the VM is functional:

-   **1 = available**
-   **0 = unavailable**

------------------------------------------------------------------------

### 3️⃣ Creating the Alert Rule

Using the metric chart:

-   Selected **New alert rule**
-   Navigated to the **Condition** tab
-   Configured logic to detect VM downtime

#### 📌 Alert Logic Configuration

  Setting            Value
  ------------------ -----------
  Threshold          Static
  Aggregation Type   Average
  Operator           Less than
  Unit               Count
  Threshold Value    1

➡️ **Meaning:** Trigger an alert when the VM's availability is **\< 1**,
indicating downtime.

------------------------------------------------------------------------

### Check Frequency

  Setting           Value
  ----------------- ----------
  Check Every       1 minute
  Lookback Period   1 minute

This ensures rapid detection.

------------------------------------------------------------------------

### 4️⃣ Creating the Action Group

To receive real-time notifications:

-   Opened **Notifications → Create Action Group**

**Configured:**

  Action Group Settings   Value
  ----------------------- ------------------------------------------
  Name                    VM-Unavailability-Alert
  Display Name            VM Unavailable
  Notification Type       SMS / Email
  Audience                Phone number & email used in the project

Action Groups ensure alerts are routed to individuals or teams
immediately.

------------------------------------------------------------------------

### 5️⃣ Finalizing the Alert Rule

Set alert details:

  Setting           Value
  ----------------- ----------------------------------------
  Severity          Based on preference (e.g., Sev 2 or 3)
  Alert Rule Name   VM Unavailability
  Description       Triggers when a VM becomes unavailable

Then: - Reviewed settings\
- Saved the alert rule

------------------------------------------------------------------------

## 📊 Outcome

The VM availability monitoring pipeline provides:

✔ Automated alerting for VM downtime\
✔ 1-minute detection frequency\
✔ Immediate SMS/email notifications\
✔ Improved operational visibility\
✔ Faster response to service outages\
✔ Support for cloud business continuity

This strengthens the overall operational resilience of cloud workloads.

------------------------------------------------------------------------

## 📁 Related Files

-   **Alert-Rule-Config.md**\
-   **Action-Group-Setup.md**\
-   **Notes.md**
