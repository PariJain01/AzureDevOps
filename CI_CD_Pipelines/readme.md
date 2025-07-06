## Task 7: Apply Triggers in Build and Release Pipelines

### 🔹 Objective
Configure Continuous Integration (CI) and Continuous Deployment (CD) triggers for automated builds and releases.

---

### ✅ 1. CI Trigger in Build Pipeline
The build pipeline was configured to trigger automatically on push to `master` and `develop` branches.

```yaml
trigger:
  branches:
    include:
      - master
      - develop
