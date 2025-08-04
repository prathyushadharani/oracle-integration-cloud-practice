# Module 9: Build Complex Journal Import Integration – App-Driven Orchestration Style

## 🔧 Use Case
Import journal entries into **ERP Cloud** using web services. The flow includes:
- Trigger: REST Adapter (e.g., "Import Journal" request)
- Invoke: ERP SOAP Adapter or External API
- Features: Loops, Scopes, Error Handling, Notifications

---

## 🔑 Key Topics Covered
- Using **App-Driven Orchestration** for complex service integration
- Advanced **Mapping** and transformations
- Implementing:
  - **Scope** (group steps)
  - **Loops** (for multi-records)
  - **Fault Handlers** (to manage errors gracefully)
  - **Notification Step** (e.g., send email on failure/success)
- ERP Cloud adapter invocation pattern

---

## 🧠 My Notes
- **Scopes** help isolate parts of integration (like Try-Catch)
- **Fault Handlers** within scopes can capture and route errors
- Use **Notifications** to email status to end-users or support team
- Mapping becomes complex with nested structures — plan payloads carefully

---

## 🧪 What I Did in the Lab
- [ ] Created integration `JournalImportFlow`
- [ ] Designed trigger (REST) and ERP Adapter as invoke
- [ ] Wrapped invoke logic in a Scope
- [ ] Created a Fault Handler to send failure notifications
- [ ] Sent email confirmation using Notification action
- [ ] Tested successful and failed journal submissions

---

## 📎 Sample Payload (Input)
```json
{
  "journalId": "JRNL1001",
  "lines": [
    {"account": "1001", "amount": 500},
    {"account": "2001", "amount": -500}
  ]
}
