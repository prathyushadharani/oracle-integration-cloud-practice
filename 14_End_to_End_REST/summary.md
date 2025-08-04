# Module 14: End-to-End Real-Time Integration (REST to ERP with Fault Handling)

## 🔧 Use Case
This module demonstrates a **real-time integration** scenario where a REST API receives input from an external system (like Salesforce or a web portal), and triggers a transaction in Oracle ERP Cloud — such as creating an invoice, customer, or purchase order.

This flow is fully **App-Driven**, and includes:
- REST Inbound Trigger
- ERP Adapter (outbound)
- Fault Handling + Logging + Notification

---

## 🔑 Key Topics Covered
- Exposing a REST API using REST Adapter (App-Driven flow)
- Mapping external input (JSON) to ERP-required format
- Invoking Oracle ERP Cloud services using ERP Adapter
- Handling ERP errors via Fault Handler
- Logging and sending email alerts on failures
- Using tracking variables and business identifiers

---

## 🧠 My Notes
- Input structure must be validated at entry (you can use an IF condition or XSLT)
- ERP Adapter needs **security configuration** (pre-set in lab)
- When invoking ERP service, use correct WSDL (e.g., ARInvoiceService)
- Store request/response payloads in variables for logging
- Use Fault Handler to:
  - Log ERP fault response
  - Send an email using Notification or a standalone integration
- Use Business Identifiers (like invoice number) for easier tracking in Monitoring

---

## 🧪 What I Did in the Lab
- [x] Created integration: `Create_AR_Invoice_REST`
- [x] REST Adapter → receives invoice input
- [x] ERP Adapter → invokes `createARInvoice` web service
- [x] Used Assign actions to format payload
- [x] Used Fault Handler to catch and log error
- [x] Called `Send_Email_Alert` integration (from Module 13) in fault path

---

## ✉️ Sample Input Payload (REST POST)
```json
{
  "customerName": "Sundar Metals",
  "invoiceAmount": 785.50,
  "invoiceDate": "2025-08-04",
  "currency": "USD"
}
```
##  📎 Screenshot Ideas
REST Adapter configuration (exposed URL and structure)

ERP Adapter config (with Operation & Credentials)

Request payload mapping (Assign step before ERP call)

Fault handler design: scope, error log, email call

Instance trace showing successful or failed ERP call

##  🗂️ Save all screenshots in:
14_End_to_End_REST/artifacts/

##  📌 Summary
This integration shows how OIC can act as a real-time API gateway between third-party apps and Oracle ERP. It captures the end-to-end business scenario, includes fault resilience, and shows how to trigger downstream flows like notifications — an essential pattern in production systems.

---

## 🔗 Helpful References

- 📘 [Using ERP Adapter in Oracle Integration Cloud](https://docs.oracle.com/en/cloud/paas/integration-cloud/erp-adapter/index.html)  
- 🔐 [Setting Up ERP Adapter Security – Oracle Docs](https://docs.oracle.com/en/cloud/paas/integration-cloud/using-integrations/credentials-erp.html)  
- 📤 [Create AR Invoice – ERP SOAP WSDL & Reference](https://docs.oracle.com/en/cloud/saas/financials/23d/farws/api-invoice-service.html)  
- 🧾 [How to Use Business Identifiers in OIC](https://docs.oracle.com/en/cloud/paas/integration-cloud/integrations-user/track-integration-instances.html#GUID-8AFDAB88-EAB0-4B4A-BF9D-9A5426BB8A2C)  
- 🪓 [Fault Handling Best Practices in OIC](https://docs.oracle.com/en/cloud/paas/integration-cloud/integrations-user/fault-handling.html)


