# Alert Rule Configuration -- Azure VM Availability Monitoring

This document outlines the configuration details for the **VM
Availability Alert Rule** created in Azure Monitor.\
The alert rule detects when a virtual machine becomes unavailable and
triggers an immediate notification via the associated Action Group.

------------------------------------------------------------------------

## 📌 Objective of the Alert Rule

To detect VM downtime in real-time and automatically notify
stakeholders, ensuring high availability and incident response
readiness.

This rule uses the **VM Availability Metric (Preview)** and triggers
when availability falls below an acceptable threshold.

------------------------------------------------------------------------

## ⚙️ Alert Rule Details

### **Alert Rule Name:**

**VM Unavailability**

### **Description:**

Triggers when the selected virtual machine's availability drops below
**1** (indicating the VM is not functional).

### **Resource:**

Azure Virtual Machine (**IPO-VM** or selected VM)

### **Severity:**

Configurable --- typically **Sev 2** or **Sev 3**

-   **Sev 2:** High priority\
-   **Sev 3:** Medium priority

------------------------------------------------------------------------

## 📊 Condition Configuration

The rule's condition is based on the **VM Availability Metric**.

### **Metric:**

VM Availability Metric (Preview)

### **Logic Configuration**

  Setting            Value
  ------------------ -----------
  Threshold          Static
  Aggregation Type   Average
  Operator           Less than
  Threshold Value    1
  Unit               Count

### **Explanation:**

-   Azure returns **1** when the VM is available\
-   Returns **0** when unavailable\
-   The alert triggers when the **average availability value \< 1**

------------------------------------------------------------------------

## ⏱ Evaluation Settings

  Setting           Value
  ----------------- ----------
  Check Every       1 minute
  Lookback Period   1 minute

These settings ensure rapid detection and minimal downtime before
alerting.

------------------------------------------------------------------------

## 📨 Actions

This alert rule is linked to an **Action Group** to deliver
notifications.

### **Action Types:**

-   Email\
-   SMS\
-   Push\
-   Voice

### **Examples:**

-   SMS alert to admin phone number\
-   Email alert to operations mailbox

Action Groups ensure uninterrupted notification delivery.

------------------------------------------------------------------------

## 🧾 Details Tab Configuration

  Field             Value
  ----------------- --------------------------------------------------
  Subscription      Selected subscription used for the VM
  Resource Group    Resource group where the VM resides
  Alert Rule Name   VM Unavailability
  Description       Trigger alert when VM availability drops below 1
  Enabled           Yes

------------------------------------------------------------------------

## 📝 Final Review & Creation

Actions performed before saving the rule:

-   Verified threshold values\
-   Confirmed selected VM and metric\
-   Checked Action Group assignments\
-   Validated severity and naming conventions

After confirmation, the rule was **saved and successfully activated**.

------------------------------------------------------------------------

## 🎯 Outcome & Impact

The VM availability alert rule provides:

✔ Immediate visibility into VM outages\
✔ Automated downtime notifications\
✔ Better operational awareness\
✔ Faster troubleshooting response times\
✔ Strong support for uptime monitoring & service readiness

This strengthens the reliability and resilience of cloud infrastructure.

------------------------------------------------------------------------

## 📁 Related Files

-   **VM-Monitoring-Overview.md**\
-   **Action-Group-Setup.md**\
-   **Notes.md**
