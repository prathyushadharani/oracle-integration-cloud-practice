# Module 4: Web Services Basics – SOAP & REST in OIC

## 🔑 Key Topics Covered
- What are Web Services?
- **SOAP Basics**
  - WSDL (Web Services Description Language)
  - Envelope, Header, Body structure
  - Strong typing and XML-based payloads
- **REST Basics**
  - JSON payloads
  - Stateless communication
  - Methods: GET, POST, PUT, DELETE
- Testing:
  - SOAP using SOAP UI/Postman
  - REST using Postman
- Oracle ERP Standard Services:
  - Sample SOAP: ERP Integration Service
  - Sample REST: ERP Bank Accounts API

## 🧠 My Notes
- SOAP is still widely used in Oracle ERP services (e.g., FBDI Uploads, Invoices)
- WSDL defines all operations, input/output structure — required for using SOAP Adapter
- REST is easier to test and lighter for performance
- OIC supports both adapters and works well in hybrid flows (e.g., REST trigger → SOAP invoke)

## 🧪 What I Practiced
- [ ] Tested a SOAP WSDL using SOAP UI/Postman
- [ ] Called a public REST API using Postman
- [ ] Compared SOAP vs REST payloads

## 📌 Summary
This module clarified the foundational differences between SOAP and REST — both are key in Oracle Cloud integrations. Knowing when to use each helps design better integration patterns.

## 📎 Sample Payload (REST - ERP Banks)
```json
{
  "BankName": "ABC Bank",
  "BankNumber": "123456789"
}
