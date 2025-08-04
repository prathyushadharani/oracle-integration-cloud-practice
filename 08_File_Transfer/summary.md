# Module 8: Build File Transfer Integration – Scheduled Orchestration Style

## 🔧 Use Case
Build a **Scheduled Orchestration** that transfers files from one location (e.g., FTP/SFTP or staging) to another:
- Trigger: Scheduler (runs at specific time)
- Invoke: File/FTP Adapter
- Optional: PGP encryption/decryption
- Goal: Move or process files in a secure, automated way

---

## 🔑 Key Topics Covered
- Scheduled Integration setup and **timing options**
- Using **File Adapter** for read/write operations
- Using **FTP Adapter** for remote transfers
- Setting up **PGP Encryption/Decryption**
- Activating, scheduling, and **monitoring file-based runs**
- File content handling: XML, CSV, fixed-width

---

## 🧠 My Notes
- Scheduled integrations don’t require external triggers (no REST/SOAP call)
- File Adapter can:
  - Read files from a directory
  - Write files to a target path
- FTP Adapter supports secure file transfers (SFTP/FTPS)
- PGP is optional but used for security in file transfers

---

## 🧪 What I Did in the Lab
- [ ] Created `FileTransferDemo` with Scheduled trigger
- [ ] Used File Adapter to pick file from input directory
- [ ] Wrote file to FTP folder using FTP Adapter
- [ ] Added basic tracking to monitor run history
- [ ] Scheduled to run every 5 minutes and tested with sample CSV

---

## 📎 File Structure Example
Input file:
