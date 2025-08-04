# Module 6: Build First REST API – App-Driven Orchestration Style

## 🔧 Use Case
Build a simple REST-to-REST integration using the **App-Driven Orchestration** style:
- Trigger: REST Adapter (e.g., POST /greet)
- Invoke: Another REST Adapter or Echo-like response
- Flow: Accept a name in the input, return a custom greeting in output

---

## 🔑 Key Topics Covered
- App-Driven Orchestration Style
- Using REST Adapter as a **trigger** and **invoke**
- Enabling **tracking fields** for monitoring
- Defining **request/response payloads**
- Message **mapping editor** in OIC
- Activating and **testing** your integration
- Monitoring instance logs

---

## 🧠 My Notes
- Use **JSON samples** to auto-generate schemas
- You must **enable tracking fields** during creation (e.g., “name” or “id”)
- Mapping editor supports drag-and-drop + XPath functions
- Test payload example:
```json
{
  "name": "Prathyusha"
}
