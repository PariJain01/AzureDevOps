# Azure DevOps Assignment

This repository documents the completion of an Azure DevOps assignment with all required tasks implemented using Azure DevOps tools and pipelines.

---

## Create a Project with Different User Groups and Implement Group Policies

- Created a new Azure DevOps project
- Created different user groups (e.g., Admins, Developers, Testers)
- Assigned users to each group
- Applied permissions and group-level policies

---

##  Apply Branch Policies to Restrict Access to the Master Branch

- Enforced branch policies on the `main` branch
  - Minimum number of reviewers
  - Work item linking
  - Comment resolution before merge
  - Restriction on direct push

---

##  Apply Branch Security and Locks

- Configured branch-level security:
  - Contributors: Denied Contribute and Force Push
  - Project Admins: Allowed
- Locked the master branch to prevent any updates temporarily

---

##  Apply Branch Filters and Path Filters

- Applied branch filters to target only specific branches like `master` and `develop`
- Configured path filters to enforce policies only on changes within specific folders (e.g., `/src/`, `/docs/`)

---

## Apply a Pull Request

- Created a feature branch and made a change
- Opened a pull request targeting `master`
- Reviewed and approved the PR
- Completed the PR using Squash Merge as per policy

---

##  Apply Branch Security for Pull Requests Only

- Ensured that contributors can create pull requests but cannot push or merge directly to `master`
- Confirmed:
  - Contributors: Denied direct push permissions
  - Pull requests required with approvals for merging

---

## Apply Triggers in Build and Release

### CI Trigger (Build Pipeline)

Configured a YAML pipeline to automatically run builds on push to `master` and `develop` branches.

```yaml
trigger:
  branches:
    include:
      - master
      - develop

pool:
  vmImage: 'ubuntu-latest'

steps:
  - task: NodeTool@0
    inputs:
      versionSpec: '16.x'
    displayName: 'Install Node.js'

  - script: |
      npm install
      npm run build
    displayName: 'Install dependencies and build'

  - script: npm test
    displayName: 'Run tests'
````

### CD Trigger (Release Pipeline)

* Created a release pipeline linked to the build artifact
* Enabled continuous deployment trigger
* Release triggered automatically after successful build

---

## Apply Gates to the Pipeline

* Configured gates in the release pipeline using “Query Work Items”
* Set the gate to require that all linked bugs are resolved before deployment
* Release paused until the gate condition was satisfied

---

## 📌 Final Summary

* Secured the project using proper user roles and permissions
* Configured strict branch protection rules
* Enforced pull requests and peer reviews
* Automated build and deployment using triggers
* Applied pre-deployment gates for release validation
* All steps completed and verified through Azure DevOps UI and pipelines
