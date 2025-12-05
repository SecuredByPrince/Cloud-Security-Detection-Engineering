# Action Group Setup — Azure VM Availability Monitoring

This document describes the steps used to configure an **Action Group** in Azure Monitor to send real-time notifications (SMS/email) whenever the VM Availability alert fires.

## 📌 Objective

Create an Action Group that:
- Sends **SMS and/or email notifications**
- Alerts the subscriber instantly when the monitored VM becomes unavailable
- Integrates with the Azure Monitor **VM Availability Metric** alert rule

This Action Group is linked to the alert rule defined in `Alert-Rule-Config.md`.

## 🛠 Steps to Create an Action Group

### 1️⃣ Navigate to Azure Monitor

1. Sign in to the **Azure Portal**  
2. In the global search bar, search for **Monitor**  
3. Select **Monitor → Alerts → Action groups**

---

## 2️⃣ Create a New Action Group

Click **Create action group**.

---

## 🔹 A. Basics Tab

### Project Details

| Setting | Value |
|--------|--------|
| Subscription | Select your subscription |
| Resource Group | Select the resource group for the action group |
| Region | Select the same region as the alert rule |

### Instance Details

| Field | Value |
|-------|--------|
| Action Group Name | `VM-Unavailability-Alert` |
| Display Name | `VM Unavailable` |

Click **Next: Notifications**.

---

## 🔹 B. Notifications Tab

### Add Notification Type

1. From **Notification type**, select:  
   **Email/SMS message/Push/Voice**
2. Choose **SMS**, and optionally **Email**

### Enter Contact Details

- Add the **phone number** for SMS alerts  
- Add **email** if needed  
- Name the contact (e.g., `Primary-Contact`)

Click **OK**, then **Review + create**.

---

## 🔹 C. Review & Create Tab

Review:
- Action group name  
- Notification types  
- Recipient contact info  

Click **Create**.

---

## 📤 Action Group Output Summary

| Component | Value |
|----------|--------|
| Action Group Name | VM-Unavailability-Alert |
| Display Name | VM Unavailable |
| Notification Types | SMS (+ optional Email) |
| Purpose | Notify stakeholder when VM availability drops below 1 |

---

## 📁 Related Files

- VM-Monitoring-Overview.md  
- Alert-Rule-Config.md  
- Notes.md
