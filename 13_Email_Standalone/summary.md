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

---

## 📎 Screenshot Ideas

These are the screenshots I plan to capture and save in the `artifacts/` folder:

1. **Notification action config** – how the notification step is configured inside the integration
2. **Email body HTML formatting with variable mapping** – where dynamic values like `message`, `error code`, and `timestamp` are injected
3. **Postman request and successful email preview** – input payload and actual received email

🗂️ These will be stored in:  
`13_Email_Standalone/artifacts/`

---

## 📌 Summary

Creating a **dedicated email integration** is a best practice in OIC.

- 🔁 **Reusable** across multiple flows for alerting and notifications
- 💬 Accepts **dynamic inputs** like subject, recipient, and message body
- 📧 Supports **HTML-formatted content** in emails
- 🚨 Adds professional-grade error monitoring to scheduled and app-driven flows

---

## 🔗 Helpful References

- 📘 [Using Email Notification in OIC – Oracle Docs](https://docs.oracle.com/en/cloud/paas/integration-cloud/integrations-user/using-notification-action.html)  
- 🧾 [HTML Tags Supported in Email Body – W3Schools](https)
