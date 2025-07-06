# Apply Branch Security and Locks

### 🔹 Objective
Secure the master branch by:
- Validating permissions
- Locking the branch to prevent any updates

---

### ✅ 1. Verified Branch Security
Confirmed that permissions are applied as follows:

| Group                  | Contribute | Force Push |
|------------------------|:----------:|:----------:|
| Project Administrators | ✅ Allow   | ✅ Allow   |
| Contributors           | ❌ Deny    | ❌ Deny    |

![Branch Security](./screenshots/07_Branch_Security_Verified.png)

---

### ✅ 2. Branch Lock
The master branch was locked to prevent any pushes or merges by any user.

This is used to protect the branch during critical periods (e.g., production releases).

---

### 📌 Summary
The master branch is now:
- Protected by strict permissions
- Locked to block all contributions temporarily
- Ready for secure development workflows

---
