## Apply Gates to the Pipeline

### 🔹 Objective
Configure gates in the release pipeline to ensure deployments proceed only after automated validations succeed.

---

### ✅ 1. Gate Configuration
The release pipeline pre-deployment conditions were configured with the following gate:

**Gate Type:**
- Query Work Items

**Criteria:**
- All linked work items must be in a Resolved or Closed state.

---

### ✅ 2. Gate Execution
During release creation, the pipeline paused and waited for the gate evaluation to succeed before starting deployment.

---

### 📌 Summary
This demonstrates the ability to:
- Enforce automated validations before deployments.
- Integrate Azure Boards work items with release gates.
- Implement a controlled deployment workflow.

---
