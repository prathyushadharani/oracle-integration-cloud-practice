# Module 12: Advanced Exception Handling with Retry Logic (Scheduled Orchestration)

## 🔧 Use Case
In real-world batch jobs (like FBDI imports), errors like missing files, FTP failures, UCM unavailability, or ERP job rejection are common. This module teaches how to:
- Detect failures
- Retry safely
- Send alerts (email, log, or dashboard)

---

## 🔑 Key Topics Covered
- Using **Scope** and **Fault Handler** in scheduled integrations
- Implementing **Retry Mechanism** using:
  - JavaScript counter
  - Wait/Delay action
  - Do-until loop (in versions that support it)
- Sending custom error emails
- Logging meaningful error messages
- Exit gracefully when retries fail

---

## 🧠 My Notes
- Scheduled integrations can’t use Fault Handlers the same way as App-Driven ones — must handle inside the **main flow**
- Use a **JavaScript counter** to control retries (max 3, with delays)
- Log each failure attempt and final outcome
- Use **email templates** to notify admin/IT teams of failure or retry exhaustion
- Wrap FTP read + ERP upload + ESS job inside a **Scope**, so any part can trigger the fault path

---

## 🧪 What I Did in the Lab
- [x] Created integration `FBDI_Customer_Import_Retry`
- [x] Added error-prone steps inside Scope (e.g., read FTP, upload to UCM)
- [x] Created `retryCount` variable with JavaScript
- [x] Used `while` loop with wait (5s) between each retry
- [x] On final failure, logged the error and sent email notification
- [x] Validated with a missing file scenario to test retry + exit

---

## 📎 Screenshot Ideas
- Retry loop setup with variable increment
- Fault flow with alert email action
- Scope + Catch configuration
- Audit trail showing retries

---

## 🧾 Sample Failure Scenario to Test

FTP file not found → Retry 3 times → Still fails → Log error → Send email → Exit


---

## 📌 Summary
This module brings real robustness to batch processes. Instead of failing silently or crashing, your integration now tries again, logs why it failed, and alerts the right team. These are **enterprise-grade skills** that clients expect from professional OIC developers.

---

## 🔗 Helpful References
- [Handling Faults in Scheduled Integrations – Oracle Docs](https://docs.oracle.com/en/cloud/paas/integration-cloud/integrations-user/handle-errors-integration.html)
- [Using JavaScript in OIC – Official Guide](https://docs.oracle.com/en/cloud/paas/integration-cloud/integrations-user/using-javascript-action.html)
