# 🗂️ Artifact Upload Guide (Per Module)

This document explains what to store inside the `artifacts/` folder of each module. These files help in revision, interviews, and showing real effort.

---

## ✅ What Goes Inside artifacts/ Folder?

| File Type           | File Name Example            | Purpose                                           |
|---------------------|------------------------------|---------------------------------------------------|
| 🖼️ Screenshots       | `designer-page.png`           | Show main integration setup                       |
| 🧩 Mappings          | `rest-to-soap-map.png`        | Visual proof of field mapping                     |
| 🛠️ Error Logs        | `fault-tracking-error.png`    | For modules with fault handlers                   |
| 📄 Sample Payloads   | `input-payload.json`          | Request sent via Postman                          |
| 📥 Input Files       | `invoice_input.csv`           | FBDI / file-based use cases                       |
| 📤 Output Files      | `invoice_output.json`         | Show formatted response from ERP Cloud            |

---

## 📎 Best Practices
- Use clear, short filenames (e.g., `mapping.png`, `payload.json`)
- Add a `readme.md` inside the `artifacts/` folder if the module is complex
- Upload screenshots immediately after completing the module

---

## 📝 Tip
If GitHub doesn’t let you create an empty folder, create a placeholder file named `.gitkeep` inside `artifacts/` so it stays visible in the repo.

