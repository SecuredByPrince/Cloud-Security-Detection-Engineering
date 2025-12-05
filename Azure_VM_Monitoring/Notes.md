# Notes — Azure VM Availability Monitoring

This file contains important notes, observations, and reminders gathered during the configuration and testing of the Azure VM Availability Monitoring pipeline.

## 📝 General Notes

- The monitoring setup uses the **VM Availability Metric (Preview)**, which reports VM uptime as:
  - **1 = Available**
  - **0 = Unavailable**
- Alerts are generated based on the **Metric Alerts** engine in Azure Monitor.
- Ensure the target VM is located within a supported region for the metric.
- The VM used for this project: **IPO-VM**

## ⚙️ Alert Rule Notes

- The alert logic was configured to trigger when **Average < 1**, indicating VM downtime.
- Evaluation frequency was set to:
  - **Check every:** 1 minute  
  - **Lookback period:** 1 minute  
- Frequent checks ensure near real-time detection of failures.
- Severity can be customized (e.g., **Sev 2** or **Sev 3**) based on operations policy.

## 📡 Action Group Notes

- Action group name: **VM-Unavailability-Alert**
- Display name: **VM Unavailable**
- Notification channel used: **SMS** (email optional)
- SMS notifications deliver faster awareness for downtime events.
- Phone numbers must be verified and allowed for the selected Azure region.

## 🔍 Testing & Validation Notes

- After setup, validation was performed to confirm:
  - The alert rule appears in **Monitor → Alerts → Alert rules**
  - The action group appears in **Monitor → Alerts → Action groups**
  - The VM availability metric visualizes correctly in Azure Monitor
- Full downtime testing requires stopping or deallocating the VM.

## 🧩 Troubleshooting Notes

- **No alerts received?**  
  - Check if the VM availability metric displays any **0** values.  
  - Confirm action group notifications are enabled.
  - Ensure phone number format follows expected international format.
- **Alert rule not firing?**  
  - Review thresholds and metric conditions.  
  - Ensure the alert rule is enabled.
- **Delayed notifications?**  
  - Check Azure Monitor service health.  
  - Validate SMS provider in your region.

## 📁 Related Project Files

- VM-Monitoring-Overview.md
- Alert-Rule-Config.md
- Action-Group-Setup.md
