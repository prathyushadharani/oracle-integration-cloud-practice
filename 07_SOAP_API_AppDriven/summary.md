# Module 7: Build First SOAP Service – App-Driven Orchestration Style

## 🔧 Use Case
Build an App-Driven integration using **SOAP Adapter** to invoke a SOAP web service:
- Trigger: REST or SOAP Adapter
- Invoke: SOAP Adapter using a public or ERP WSDL
- Flow: Accept input, pass it to SOAP request, return the response

---

## 🔑 Key Topics Covered
- What is **SOAP Adapter** and how to configure it
- How to use **WSDL** to generate the SOAP service definition
- Enabling **tracking fields** for monitoring
- Message **mapping** between REST/SOAP formats
- Activating, testing, and **monitoring** SOAP integrations

---

## 🧠 My Notes
- SOAP Adapter requires a **WSDL URL or file** — no WSDL, no adapter!
- It auto-generates operations and schema for mapping
- Input/output is in **XML structure** (vs JSON for REST)
- You can test public SOAP services like:
  - http://www.dneonline.com/calculator.asmx?wsdl

---

## 🧪 What I Did in the Lab
- [ ] Created App-Driven integration named `InvokeCalculatorSOAP`
- [ ] Used Calculator WSDL for invoke adapter
- [ ] Mapped two numbers as input to SOAP
- [ ] Returned sum result from SOAP response
- [ ] Enabled tracking and tested via Postman

---

## 📌 Sample Flow: REST to SOAP
```json
// REST Input
{
  "num1": 5,
  "num2": 3
}
