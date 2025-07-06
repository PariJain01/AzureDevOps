### 🔹 Objective
To create a new Azure DevOps project, define multiple user groups, assign users to those groups, and apply appropriate group-level policies and permissions.

---

### ✅ 1. Project Creation
A new Azure DevOps project named `DevOpsAssignment` was created with the following details:
- **Visibility:** Private
- **Version Control:** Git
- **Work Item Process:** Agile

---

### ✅ 2. Custom User Groups
The following user groups were created under the **Project Settings > Permissions** section:
- **Developers**
- **Testers**
- **Release Managers**

Each group was created to manage access control and role separation within the project.

---

### ✅ 3. Adding Members to Groups
Test users or my own email account were added to the newly created groups to simulate group membership.

---

### ✅ 4. Group Permissions & Policies
Permissions were configured for each group to enforce access control:

- **Developers**
  - Contribute: ✅ Allowed
  - Delete repository: ❌ Denied
  - Edit policies: ❌ Denied

- **Testers**
  - View code: ✅ Allowed
  - Contribute: ❌ Denied
  - Comment on pull requests: ✅ Allowed

- **Release Managers**
  - View pipelines: ✅ Allowed
  - Manage releases: ✅ Allowed
  - Approve deployments: ✅ Allowed

These permissions were applied through **Project Settings > Repositories** and **Pipelines**.

---

### 📌 Summary
The task demonstrates understanding of:
- Setting up an Azure DevOps project
- Managing users and groups
- Implementing RBAC (Role-Based Access Control) through permissions

---
