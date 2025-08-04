# Module 10: Build Complex AR Invoice REST API – App-Driven Orchestration Style

## 🔧 Use Case
Design a single App-Driven integration with **multiple REST endpoints** to:
1. **GET** AR Invoice details from ERP Cloud
2. **POST** new AR Invoice to ERP Cloud

---

## 🔑 Key Topics Covered
- Creating multiple **REST resources (GET & POST)** in one integration
- Understanding how to use **REST triggers** for both read and create operations
- Using **ERP Cloud Adapter** to:
  - Invoke **seeded ERP REST APIs**
  - Map data to/from ERP fields
- Handling headers, payloads, and status codes

---

## 🧠 My Notes
- One integration can have multiple endpoints like:
  - `GET /invoices/{invoiceId}`
  - `POST /invoices`
- ERP REST APIs are easier than SOAP for AR modules
- Headers (like `Content-Type`) and query parameters should be handled carefully
- Response must include proper HTTP status codes (200, 201, 400)

---

## 🧪 What I Did in the Lab
- [ ] Created integration `ARInvoiceFlow`
- [ ] Defined GET and POST operations using REST trigger
- [ ] Used ERP Adapter to fetch and create invoice in Oracle SaaS
- [ ] Mapped input and output payloads for both resources
- [ ] Tested in Postman with sample data

---

## 📎 Sample Payloads

**POST /invoices**
```json
{
  "customerId": "CUST1001",
  "amount": 1500,
  "currency": "USD"
}
