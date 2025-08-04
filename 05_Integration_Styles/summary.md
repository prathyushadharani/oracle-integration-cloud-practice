# Module 5: Introduction to Integrations in Oracle Integration Cloud (OIC)

## 🔑 Key Topics Covered
- Core components of an OIC Integration:
  - Trigger
  - Invoke
  - Mapping
  - Error Handling
  - Tracking
- **Integration Development Workflow**:
  1. Design
  2. Activate
  3. Test
  4. Monitor
- **6 Integration Styles in OIC**:
  1. **App-Driven Orchestration**
  2. **Scheduled Orchestration**
  3. **File Transfer**
  4. **Basic Routing**
  5. **Publish to OIC**
  6. **Subscribe to OIC**
- When to use each style
- Trigger & Invoke Adapters — REST, SOAP, File, FTP, Email, DB, etc.

## 🧠 My Notes
- App-Driven is used when a flow is triggered by an external system (e.g., REST call)
- Scheduled is best for batch jobs like FBDI, or polling files
- File Transfer is limited — mainly for file movement tasks
- Publish/Subscribe is used in event-driven architectures

## 🧪 What I Did
- [ ] Reviewed the designer UI to explore integration styles
- [ ] Explored adapter configuration options (e.g., REST vs SOAP)
- [ ] Noted trigger/invoke adapter behavior during testing

## 📌 Summary
This module explained the core structure and types of integrations in OIC. Understanding these styles is critical before building your first REST API flow.

## 📝 Questions to Self
- When should I use Scheduled vs App-Driven?
- How do error handlers differ across integration types?

## 🔗 Useful References
- [Oracle Integration Styles – Official Docs](https://docs.oracle.com/en/cloud/paas/integration-cloud/integrations-user/integration-style-overview.html)
