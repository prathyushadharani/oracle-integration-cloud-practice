# Module 11: Build FBDI Automation Integration – Scheduled Orchestration Style

## 🔧 Use Case
Automate the end-to-end process of **FBDI-based data import** (e.g., Customers, Journals, Invoices) into Oracle ERP Cloud using scheduled orchestration.

Steps typically include:
1. **Pick file** (CSV/XML) from FTP/SFTP
2. **Stage the file** in UCM (ERP cloud)
3. **Call ERP Import Job** (via SOAP/REST)
4. **Track results** and send notifications

---

## 🔑 Key Topics Covered
- Working with **Scheduled Integrations**
- Reading files using **FTP/File Adapter**
- Uploading to **ERP UCM** using ERP Adapter
- Invoking **ESS Job** (ERP process like "Import Journals")
- Tracking ESS status and logging success/failure
- (Optional) **Email Notification** with status + file info

---

## 🧠 My Notes
- FBDI = File-Based Data Import
- UCM is Oracle's cloud document repository for ERP uploads
- ERP Adapter is used both for UCM and for triggering ESS jobs
- ESS Job names and parameters vary by module (e.g., CustomerImport, JournalImport)
- Mapping ESS request is tricky: follow exact structure (reqName, parameter list)

---

## 🧪 What I Did in the Lab
- [ ] Created integration `FBDI_Customer_Import`
- [ ] Triggered by Scheduler every 5 mins
- [ ] Read file `customer_import.csv` from FTP folder
- [ ] Uploaded file to UCM with metadata: title, docAccount, type
- [ ] Invoked ESS job: `ImportCustomerFBDI`
- [ ] Monitored job status and wrote result to log
- [ ] (Optional) Sent status email to support team

---

## 🧾 Sample File Content (customer_import.csv)
CustomerNumber,CustomerName,CustomerType
CUST101,Visalaxmi Enterprises,INDIVIDUAL
CUST102,Sreya Traders,BUSINESS


---

## 📌 Summary
This integration automates a **batch data upload process** from a file drop to ERP cloud — the backbone of many real-life Oracle Fusion implementations. Mastering this flow is a must for working on Financials, SCM, HCM integrations using FBDI.

---

## 📎 Screenshot Ideas
- Scheduler page with frequency setup
- UCM upload mapping
- ESS job call configuration
- Log showing job ID and outcome

---

## 🔗 Helpful References
- [FBDI File Formats (Oracle Docs)](https://docs.oracle.com/en/cloud/saas/financials/23d/oefdi/)
- [ESS Job Names & Parameters (ERP SOAP Guide)](https://docs.oracle.com/en/cloud/saas/financials/23d/farfa/)

