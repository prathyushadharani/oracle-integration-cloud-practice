# 📚 Quick References – Oracle Integration Cloud (OIC)

Your go-to hub for documentation, URLs, WSDLs, REST API guides, XPath examples, and integration utilities. Add to this over time as you discover more!

---

## 🔗 Official Oracle Docs

- 📘 Oracle Integration Cloud Documentation (User & Admin):
  https://docs.oracle.com/en/cloud/paas/integration-cloud/index.html

- 📘 Oracle ERP Cloud (Financials) REST API Guide:
  https://docs.oracle.com/en/cloud/saas/financials/23d/farfa/

- 🔐 Oracle ERP Security & Roles Reference:
  https://docs.oracle.com/en/cloud/saas/financials/23d/fausr/security-reference-for-financials.html

- 🧾 FBDI File Formats & Templates:
  https://docs.oracle.com/en/cloud/saas/financials/23d/oefdi/

---

## 🧪 Public Sample APIs for Practice

- 🔢 Calculator SOAP WSDL:  
  http://www.dneonline.com/calculator.asmx?wsdl

- 🐱 Dummy REST API:
  https://jsonplaceholder.typicode.com/

- 📦 Sample Product JSON:  
  https://dummyjson.com/products

---

## 📤 WSDL & REST Endpoint Examples

### ERP WSDL (SOAP):)

https://<hostname>/fscmService/ErpIntegrationService?wsdl

### ERP REST Base:

https://<hostname>/fscmRestApi/resources/latest/

## 🔧 XPath Expressions (Mapping)

```xpath
concat('Hello ', $input.name)
upper-case($input.country)
if ($input.amount > 1000) then 'High' else 'Normal'
substring($input.date, 1, 10)

Postman Tips
Set Authorization → Basic Auth

Headers:

Content-Type: application/json

Accept: application/json

Export request as JSON and save in artifacts/ for traceability

 GitHub Utilities
Use .gitkeep file to create empty folders

Use Markdown checklists:

- [x] Created REST Trigger
- [ ] Add Mapping Logic



