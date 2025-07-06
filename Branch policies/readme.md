### 🔹 Objective
Configure the master branch so that only Project Administrators can push code directly, and all contributions from other users require pull requests.

---

### ✅ 1. Branch Policies Configuration
Applied the following branch policies:
- **Require minimum number of reviewers:** 1
- **Check for linked work items:** Enabled
- **Check for comment resolution:** Enabled
- **Limit merge types:** Squash merge only

These settings ensure that contributors cannot merge changes without a review process.

---

### ✅ 2. Branch Security Settings
Configured branch security permissions:

| Group                | Contribute | Force Push |
|----------------------|:----------:|:----------:|
| Project Administrators | ✅ Allow  | ✅ Allow   |
| Contributors         | ❌ Deny    | ❌ Deny    |

This restricts direct pushes to Project Administrators only.


---

### 📌 Summary
This configuration ensures:
- All contributor changes are submitted via pull requests.
- Only administrators can push directly to the master branch.
- Compliance with secure development workflows.

---
