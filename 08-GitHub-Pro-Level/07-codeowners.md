
# 👥 CODEOWNERS (Code Ownership & Review Enforcement)

<p align="center">
  <img src="https://img.shields.io/badge/Level-Advanced%20%2F%20Pro-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Focus-Ownership%20%2F%20Reviews-success?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Includes-Automatic%20Reviewers-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Skill-Team%20Governance-purple?style=for-the-badge" />
</p>

<p align="center">
  <b>Automatically request reviews from the right people using CODEOWNERS — enforce accountability at scale.</b>
</p>

---

## 📌 What Is CODEOWNERS?

`CODEOWNERS` is a file that:

> Defines who owns which parts of the codebase and auto-assigns them as reviewers on Pull Requests.

---

## 🧠 Why CODEOWNERS Matters

Without ownership:

- unclear responsibility ❌
- wrong reviewers ❌
- risky merges ❌

With CODEOWNERS:

- correct reviewers auto-assigned ✅
- accountability enforced ✅
- faster, safer reviews ✅

---

## 🗺️ Big Picture

```mermaid
flowchart LR
    A[PR Opened] --> B[Changed Files]
    B --> C[Match CODEOWNERS Rules]
    C --> D[Auto-Assign Reviewers]
    D --> E[Review & Approve]
````

---

## 📂 Where to Place CODEOWNERS

GitHub checks these locations (first match wins):

```text id="own-loc"
.github/CODEOWNERS
CODEOWNERS (root)
docs/CODEOWNERS
```

👉 Best practice: use `.github/CODEOWNERS`

---

## 🧱 Basic Syntax

```text id="own-syntax"
<pattern> <owner1> <owner2>
```

* `pattern` → file/folder match
* `owner` → GitHub username or team

---

## 🧪 Examples

---

### Entire Repository Owner

```text id="own-all"
* @team-leads
```

---

### Specific Folder

```text id="own-folder"
frontend/ @frontend-team
backend/  @backend-team
```

---

### Specific File

```text id="own-file"
package.json @devops-team
```

---

### Multiple Owners

```text id="own-multi"
api/ @backend-team @tech-lead
```

---

### File Type

```text id="own-ext"
*.js @javascript-team
*.css @ui-team
```

---

## 🧠 Pattern Matching

```text id="own-patterns"
*        → everything
*.js     → all JS files
/docs/   → docs folder
/api/**  → nested folders
```

---

## 🖥️ PR UI Mock (Auto Review)

```text id="ui-own"
┌──────────────────────────────────────────────┐
│ Pull Request                                │
├──────────────────────────────────────────────┤
│ Changed: frontend/login.js                  │
├──────────────────────────────────────────────┤
│ Reviewers:                                  │
│ 👤 @frontend-team (auto-assigned)           │
└──────────────────────────────────────────────┘
```

---

## 🔄 How It Works (Step-by-Step)

```text id="own-flow"
1. PR created
2. GitHub checks changed files
3. Matches CODEOWNERS rules
4. Assigns reviewers automatically
```

---

## 🔐 Enforcing Reviews (Branch Protection)

To make CODEOWNERS effective:

---

### Enable Branch Protection

```text id="bp1"
Settings → Branches → Protection Rules
```

---

### Enable:

```text id="bp2"
✔ Require pull request reviews
✔ Require review from Code Owners
```

---

## 🧠 Result

```text id="bp3"
PR cannot be merged without owner approval
```

---

## 🧬 Internal Flow

```text id="own-arch"
CODEOWNERS file
       │
       ▼
PR changes detected
       │
       ▼
Pattern matched
       │
       ▼
Reviewers assigned
       │
       ▼
Approval required
```

---

## 🧪 Real-World Scenario

```text id="own-real"
frontend/login.js changed
→ CODEOWNERS assigns frontend team
→ frontend team reviews
→ PR approved
→ safe merge
```

---

## ⚠️ Important Rules

---

### ❗ Last matching rule wins

```text id="own-rule"
More specific rule overrides general rule
```

---

### ❗ Owners must have access

```text id="own-access"
Users/teams must have repo permission
```

---

## 🚨 Common Mistakes

---

### ❌ Incorrect file paths

Rules won’t match.

---

### ❌ Missing permissions

Reviewers won’t be assigned.

---

### ❌ Too broad ownership

Leads to unnecessary reviews.

---

### ❌ Not enabling protection rules

No enforcement.

---

## ✅ Best Practices

* define ownership clearly
* keep rules simple
* use teams instead of individuals
* combine with branch protection
* review CODEOWNERS regularly

---

## 🧠 Pro Tips

* assign critical files to senior devs
* use teams for scalability
* separate frontend/backend ownership
* use file-type patterns for consistency

---

## 🧬 Full GitHub Workflow (Final)

```text id="full-flow"
Issue → Branch → PR → CODEOWNERS → Review → Merge → Release
```

---

## 🎤 Interview Questions

### What is CODEOWNERS?

A file that defines code ownership and auto-assigns reviewers.

---

### Where is it stored?

.github/CODEOWNERS (recommended)

---

### What does it do?

Automatically assigns reviewers based on changed files.

---

### How do you enforce it?

Using branch protection rules.

---

### Why use CODEOWNERS?

To ensure correct people review changes.

---

## 🧪 Practice Lab

---

### Task 1 — Create CODEOWNERS

```text id="lab1"
.github/CODEOWNERS
```

---

### Task 2 — Add Rules

```text id="lab2"
* @your-username
frontend/ @frontend-team
backend/ @backend-team
```

---

### Task 3 — Open PR

Modify a file → check reviewers.

---

### Task 4 — Enable Protection

Require code owner approval.

---

## 🎯 Final Takeaway

CODEOWNERS provides:

```text id="take-own"
Ownership + Accountability + Quality Control
```

It is essential for:

* large teams
* production systems
* structured reviews

---

## 👉 Next Step

➡️ `practice-lab.md`
