🛠 CRM Project – Developer Git Workflow Guide
=============================================

Welcome to the CRM project!  
To ensure smooth collaboration and clean deployment, follow this Git workflow strictly.

* * *

🌿 Branch Structure
-------------------

Branch

Purpose

`main`

🔴 **LIVE branch** – only the project owner will push here.

`production`

🟡 **Staging branch** – all PRs go here and are tested.

`dashboard`

🟢 Development for dashboard features.

`mainpage`

🟢 Development for main page features.

`feature/*`

🔧 Feature branches created from dev branches.

👨‍💻 Developer Assignments
---------------------------

Developer

Assigned Branch

Dev 1

`mainpage`

Dev 2

`dashboard`


✅ Daily Workflow Instructions
-----------------------------

### 1\. 📥 Always pull before starting work

Before writing any code, **pull the latest changes**:

    git checkout your-branch-name
    git pull origin your-branch-name

Example:

    git checkout dashboard-dev
    git pull origin dashboard-dev

### 2\. 🌿 Create a feature branch

Never work directly on dev branches. Create a new feature branch:

    git checkout -b feature/your-feature-name

Examples:

*   `feature/login-form`
*   `feature/navbar-fix`
*   `feature/mainpage-ui`

### 3\. 💻 Work, Commit, and Push

    git add .
    git commit -m "Add: implemented login form"
    git push origin feature/your-feature-name

### 4\. 🔁 Create Pull Request (PR)

Once your feature is done:

*   Go to GitHub.
*   Open a Pull Request from `feature/your-feature-name` → `production`.
*   Use a clear title and description.
*   Request a review from a teammate.

✅ **All PRs must target the `production` branch.**

### 5\. 🧪 Staging Testing

The `production` branch is your staging environment.

*   Once your PR is merged into `production`, test it thoroughly.
*   Make sure nothing breaks.
*   Ensure the UI and features work as expected.

### 6\. 🚀 Deployment to `main`

When all features in `production` are tested and confirmed:

*   The **project owner** will merge `production` → `main`.
*   This triggers deployment to live users.

⚠️ **Do not push or merge into `main` directly.**

* * *

🔒 Rules Summary
----------------

*   ✅ Always pull before working: `git pull origin your-branch`
*   ❌ Never work directly on dev branches – use feature branches.
*   ✅ Create PRs to `production`, never to `main`.
*   ❌ Do not push directly to `main`.
*   🧪 Test before requesting a merge.
*   📄 Use clear commit messages.
*   🧼 Avoid test data, logs, or unused code.

🛡 Merge Checklist Before `production` or `main`
------------------------------------------------

*   \[ \] Code runs and builds correctly.
*   \[ \] No errors or console warnings.
*   \[ \] UI is responsive and tested.
*   \[ \] Code is reviewed and approved.
*   \[ \] No test data or debug logs.
*   \[ \] PR title and description are clear."# CMR" 
