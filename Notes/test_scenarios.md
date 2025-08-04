# 🧪 Test Scenarios & Bonus Use Cases – Oracle Integration Cloud (OIC)

This document captures edge cases, sample inputs, bonus flows, and what-if scenarios for key integration styles and adapters. Use these to practice or during interviews to explain your practical understanding.

---

## 📦 App-Driven Orchestration (REST/SOAP)

### 🔁 Scenario: Simple REST Greeting Flow
- ✅ Input: `{ "name": "Sreya" }`
- ❌ Input: `{ "Name": 123 }` → Type mismatch
- ❌ Input: `{}` → Missing mandatory field
- 🔄 Loop: Try passing an array of names and build a loop to greet each

---

## 🔃 App-Driven: REST to SOAP

### 🧠 Scenario: Calculator API (SOAP)
- `intA: 5`, `intB: 3` → `Add = 8`
- `intA: 0`, `intB: 999` → Edge with zero
- `intA: "abc"` → Data type failure in SOAP Adapter

---

## ⏱️ Scheduled Orchestration

### 📁 Scenario: File Transfer
- Empty file → Should log and skip
- Incorrect file extension → Test adapter filtering
- Bad CSV headers → Mapping failure

---

## 💸 ERP Use Cases – Journal / AR Invoice

### 📘 AR Invoice POST
- ✅ Valid customer ID, currency, amount
- ❌ Missing currency field
- ❌ Negative amount → Should fail validation
- 🛡️ Security test: Try injecting script in JSON

### 📕 Journal Import
- ✅ Balanced debit/credit lines
- ❌ Unbalanced → Should error out
- ✅ Test scope retry logic (simulate temporary error)

---

## 💌 Notifications & Fault Handling

### 🔔 Test Cases
- Email on success → With dynamic message
- Email on error → Include instance ID and timestamp
- Log and continue flow vs. terminate integration

---

## 🔐 Security & Headers

- Missing Authorization header → 401
- Invalid content-type → 415
- Add static or dynamic header in REST invoke

---

## 🧪 Edge Testing Ideas

- Rapid consecutive REST calls → Test throttling
- Upload 10k rows CSV → Performance load
- Loop through 100+ JSON records using `for-each`

---

## 📌 Tip for Interviews
If asked, “How do you test your integrations?”
→ Mention you maintain this doc of test patterns, including:
- Positive and negative scenar
