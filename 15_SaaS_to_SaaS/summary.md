# Module 15: SaaS-to-SaaS Integration (ERP to HCM or CRM)

## 🔧 Use Case
In this module, we build a **real-time integration** between two SaaS systems — like Oracle ERP Cloud and Oracle HCM Cloud — to transfer data without involving file uploads or manual steps.

Typical business cases:
- Transfer employee expense data from HCM to ERP
- Sync new suppliers or projects between systems
- Push customer updates from CRM to ERP

---

## 🔑 Key Topics Covered
- SaaS-to-SaaS integration design using App-Driven flow
- Calling two different cloud systems in one flow
- ERP Adapter as source or destination
- HCM, Sales Cloud, or CX adapters
- Fault handling across chained systems
- Error isolation and notifications

---

## 🧠 My Notes
- This pattern is common in large enterprises using multiple Oracle SaaS apps
- Both SaaS adapters need **credentials & roles** (pre-configured in course lab)
- Can use **parallel flows** (if one call shouldn’t wait on the other)
- ERP Adapter typically sends/receives structured payload (XML or SOAP)
- Make sure business identifiers are unique and traceable across both calls

---

## 🧪 What I Did in the Lab
- [x] Created `Sync_HCM_to_ERP_Employee`
- [x] REST Adapter → Simulated external event
- [x] Called HCM Cloud → Get new employee
- [x] Called ERP Cloud → Create supplier record
- [x] Used Fault Handler to catch errors from either system
- [x] Logged error + sent alert using Module 13’s email integration

---

## ✉️ Sample Flow Overview
Trigger (REST)
↓
HCM Adapter → Get Employee Details
↓
ERP Adapter → Create Supplier
↓
Success or Fault Flow (log + alert)


---

## 📎 Screenshot Ideas
- HCM & ERP adapter configs
- Mapping from HCM output to ERP input
- Scope with both SaaS calls
- Monitoring page with successful tracking
- Error flow showing which system failed

🗂️ Save all screenshots in:  
`15_SaaS_to_SaaS/artifacts/`

---

## 📌 Summary
This module simulates **real-time integration across Oracle SaaS systems** — a highly demanded use case in enterprise projects. It brings together everything you've learned: REST triggers, SaaS adapters, mappings, fault handling, and reusability. It also demonstrates how OIC can act as a true middleware between business domains like HCM and Finance.

---

## 🔗 Helpful References

- 🔄 [Using Oracle ERP Adapter – Oracle Docs](https://docs.oracle.com/en/cloud/paas/integration-cloud/erp-adapter/index.html)  
- 👥 [Oracle HCM Cloud Adapter – Docs](https://docs.oracle.com/en/cloud/paas/integration-cloud/hcm-adapter/index.html)  
- 🧩 [Chaining SaaS Services in OIC](https://docs.oracle.com/en/cloud/paas/integration-cloud/integrations-user/call-another-saas-application-integration.html)  
- 📘 [Best Practices for SaaS-to-SaaS Integrations](https://blogs.oracle.com/cloud-infrastructure/post/building-saas-to-saas-integrations-on-oic)


