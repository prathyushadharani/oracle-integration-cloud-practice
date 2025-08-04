# Module 13: Email Notification + Standalone Fault Handling Integration

## 🔧 Use Case
This module introduces a **standalone integration** pattern for sending **email alerts**, which can be triggered by other integrations, or run on a schedule. Common use cases include:
- Notify users of failed jobs
- Send reports/status logs
- Manual trigger for reminder notifications

---

## 🔑 Key Topics Covered
- Designing standalone **Email Notification Integration**
- Working with the **Notification action**
- Embedding dynamic values into subject/body (from variables)
- Email formatting using HTML templates
- Reusing email integration across multiple flows
- Sending alerts based on system/ERP status

---

## 🧠 My Notes
- Email Notification integrations can be **App-Driven (for reuse)** or **Scheduled (for batch alerts)**
- Body content supports HTML — use `<br>` for new lines, `<b>` for bold, etc.
- Dynamic fields like status, timestamp, job ID can be mapped into the body
- SMTP must be configured in OIC (usually pre-configured in course environment)
- Can reuse this integration from **Fault Handler scopes** in other flows

---

## 🧪 What I Did in the Lab
- [x] Created `Send_Email_Alert` integration (App-Driven)
- [x] Took inputs: subject, recipient, message
- [x] Used Notification action to send formatted email
- [x] Tested it with Postman using mock inputs
- [x] Later used this integration inside Module 12 fault handler for failed FBDI

---

## ✉️ Sample Input Payload
```json
{
  "to": "admin@company.com",
  "subject": "🔴 FBDI Failure Alert – Customer Load",
  "message": "The customer FBDI job failed after 3 retries. Error Code: FTP404<br><br>Time: 2025-08-04 10:30 PM"
}

##  📎 Screenshot Ideas
- Notification action config

- Email body HTML formatting with variable mapping

- Postman request and successful email preview

##  📌 Summary
-  Creating a dedicated email integration is a best practice in OIC. It simplifies alerting, avoids duplication, and brings clarity in monitoring batch and real-time flows. It’s also easily callable from App-Driven or Scheduled flows.

##  🔗 Helpful References
Using Email Notification in OIC – Oracle Docs

HTML Tags Supported in Email Body
